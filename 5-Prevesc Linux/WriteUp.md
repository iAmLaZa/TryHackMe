Linux PrivEsc : 

LINK : https://tryhackme.com/room/linprivesc

What is Privilege Escalation?  

At it's core, Privilege Escalation usually involves going from a lower permission account to a higher permission one. More technically, it's the exploitation of a vulnerability, design flaw, or configuration oversight in an operating system or application to gain unauthorized access to resources that are usually restricted from the users.


Why is it important?


It's rare when performing a real-world penetration test to be able to gain a foothold (initial access) that gives you direct administrative access. Privilege escalation is crucial because it lets you gain system administrator levels of access, which allows you to perform actions such as:

	-Resetting passwords

	-Bypassing access controls to compromise protected data

	-Editing software configurations

	-Enabling persistence

	-Changing the privilege of existing (or new) users

	-Execute any administrative command

 Enumeration : 
 
 Enumeration is the first step you have to take once you gain access to any system. You may have accessed the system by exploiting a critical vulnerability that resulted in root-level access or just found a way to send commands using a low privileged account.
 
	-hostname : The hostname command will return the hostname of the target machine.
	-Uname -a : system informations 
	-/proc/version :The proc filesystem (procfs) provides information about the target system processe
	-/etc/issueSystems can also be identified by looking at the /etc/issue file
	-ps Command :The ps command is an effective way to see the running processes on a Linux system
		-ps -A: View all running processes
	-sudo -l :The target system may be configured to allow users to run some (or all) commands with root privileges. The sudo -l command can be used to list all 		commands your user can run using sudo.
	-Id :The id command will provide a general overview of the user’s privilege level and group memberships.
	-/etc/passwd :Reading the /etc/passwd file can be an easy way to discover users on the system.
	-netstat -a: shows all listening ports and established connections.
	-find / -perm -u=s -type f 2>/dev/null: Find files with the SUID bit, which allows us to run the file with a higher privilege level than the current user.

	Note: Launch the target machine attached to this task to follow along.

	You can launch the target machine and access it directly from your browser.

	Alternatively, you can access it over SSH with the low-privilege user credentials below:



	Username: karen

	Password: Password1


![1](https://user-images.githubusercontent.com/94765997/162598445-d6657534-97cc-47a9-9f6e-0f0c71e62180.png)

![2](https://user-images.githubusercontent.com/94765997/162598470-b725a23e-b8cf-41df-bb32-5faf81f1454b.png)

![3](https://user-images.githubusercontent.com/94765997/162598473-cd0de047-d76e-4069-aad0-63fb31ecaf7e.png)

![4](https://user-images.githubusercontent.com/94765997/162598475-b95a3b79-5779-4266-8f5c-c443469f6e4d.png)

![5](https://user-images.githubusercontent.com/94765997/162598482-a008acc5-4316-492e-bc2b-5f869c779a3e.png)

