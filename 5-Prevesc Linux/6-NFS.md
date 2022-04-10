Privilege escalation vectors are not confined to internal access. Shared folders and remote management interfaces such as SSH and Telnet can also help you gain root access on the target system. Some cases will also require using both vectors, e.g. finding a root SSH private key on the target system and connecting via SSH with root privileges instead of trying to increase your current user’s privilege level.

NFS (Network File Sharing) configuration is kept in the 

      /etc/exports
    
This file is created during the NFS server installation and can usually be read by users.

