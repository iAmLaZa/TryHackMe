Most of the pentesting techniques and tools you've seen so far can be used on both Windows and Linux. However, one of the things you'll find most often when pen testing Windows machines is samba, and it is worth making a section dedicated to enumerating it.



Note: Samba is cross platform as well, however this section will primarily be focused on Windows enumeration; some of the techniques you see here still apply to Linux as well.

Continuing with the trend of tools having "map" in the name being extremely popular, smbmap is one of the best ways to enumerate samba. smbmap allows pen-testers to run commands(given proper permissions), download and upload files, and overall is just incredibly useful for smb enumeration.


- [ ] How do you set the username to authenticate with?

		-u
- [ ] What about the password?    

		-p
- [ ] How do you set the host?

		-H
- [ ] What flag runs a command on the server(assuming you have permissions that is)?

		-x 
- [ ] How do you specify the share to enumerate?

		-s
- [ ] How do you set which domain to enumerate?

		-d
- [ ] What flag downloads a file?

		--download
		
- [ ] What about uploading one?

		--upload
- [ ] Given the username "admin", the password "password", and the ip "10.10.10.10", how would you run ipconfig on that machine

		smbmap -u "admin" -p "password" -H 10.10.10.10 -x "ipconfig"

smbclient allows you to do most of the things you can do with smbmap, and it also offers you and interactive prompt.


- [ ] How do you specify which domain(workgroup) to use when connecting to the host?

		-w

- [ ] How do you specify the ip address of the host?

		-I

- [ ] How do you run the command "ipconfig" on the target machine?

		-c "ipconfig"

- [ ] How do you specify the username to authenticate with?

		-U
 
- [ ] How do you specify the password to authenticate with?

		-P

- [ ] What flag is set to tell smbclient to not use a password?

		-N
	
- [ ] While in the interactive prompt, how would you download the file test, assuming it was in the current directory?

		get test

- [ ] In the interactive prompt, how would you upload your /etc/hosts file
		
		put /etc/hosts


