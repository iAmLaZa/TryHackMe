- [ ] One of the main problems of web penetration testing is not knowing where anything is.
Basic reconnaissance can tell you where some files and directories are; however, some of the more hidden stuff is often hidden away from the eyes of users.
 This is where gobuster comes in, the idea behind gobuster is that it tries to find valid directories from a wordlist of possible directories. 
gobuster can also be used to valid subdomains using the same method.


- [ ] How do you specify directory/file brute forcing mode?

		dir
- [ ] How do you specify dns bruteforcing mode?    

		dns
- [ ] What flag sets extensions to be used?

Example: if the php extension is set, and the word is "admin" then gobuster will test admin.php against the webserver

		-x
- [ ] What flag sets a wordlist to be used?

		-w
- [ ] How do you set the Username for basic authentication(If the directory requires a username/password)?

		-U
- [ ] How do you set the password for basic authentication?

		-P
- [ ] How do you set which status codes gobuster will interpret as valid?

		Example: 200,400,404,204

		-s
- [ ] How do you skip ssl certificate verification?

		-k
- [ ] How do you specify a User-Agent?

		-a
- [ ] How do you specify a HTTP header?

		-H
- [ ] What flag sets the URL to bruteforce?

		-u
Deploy the machine

![g2](https://user-images.githubusercontent.com/94765997/179360069-55fb0f04-5bce-4347-a29d-d05d087b3542.png)


- [ ] What is the name of the hidden directory
		gobuster dir -e -u http://10.10.234.146/ -w /usr/share/dirb/wordlists/common.txt

		secret
- [ ] What is the name of the hidden file with the extension xxa
		
		password
		
![g3](https://user-images.githubusercontent.com/94765997/179360078-97e4f016-a1dc-41d9-b443-96ac4cad9e8e.png)
