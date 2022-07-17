# NFS :
Privilege escalation vectors are not confined to internal access. Shared folders and remote management interfaces such as SSH and Telnet can also help you gain root access on the target system. Some cases will also require using both vectors, e.g. finding a root SSH private key on the target system and connecting via SSH with root privileges instead of trying to increase your current user’s privilege level.

NFS (Network File Sharing) configuration is kept in the 

      /etc/exports
    
This file is created during the NFS server installation and can usually be read by users.

![23](https://user-images.githubusercontent.com/94765997/162630258-17103d30-6003-4278-89d4-a6c6007e297a.png)

The critical element for this privilege escalation vector is the “no_root_squash” option you can see above. By default, NFS will change the root user to nfsnobody and strip any file from operating with root privileges. If the “no_root_squash” option is present on a writable share, we can create an executable with SUID bit set and run it on the target system.

# We will start by enumerating mountable shares from our attacking machine.

      showmount -e @ 


![22](https://user-images.githubusercontent.com/94765997/162630298-14cbfa32-de8a-46c4-b20c-25c90e646fd4.png)

      1-We will mount one of the “no_root_squash” shares to our attacking machine and start building our executable.
      2-As we can set SUID bits, a simple executable that will run /bin/bash on the target system will do the job : 
            #include <stdio.h>
            #include <stdlib.h>
            #include <unistd.h>

            int main (void){

                  setuid(0);
                  setgid(0);
                  system("/bin/bash -p");
                  return 0;
            }
      3-Once we compile the code we will set the SUID bit.
 
 ![24](https://user-images.githubusercontent.com/94765997/162630432-14aa3313-dcca-44bf-a741-8a4e521849f6.png)

  
 You will see below that both files (code.c and code are present on the target system. We have worked on the mounted share so there was no need to transfer them).
 Notice the code executable has the SUID bit set on the target system and runs with root privileges.
 
 ![25](https://user-images.githubusercontent.com/94765997/162630464-bc417857-edc5-4fca-9f08-4b9cf817fee3.png).
 
