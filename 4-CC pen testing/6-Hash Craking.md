# Intro 


Often times during a pen test, you will gain access to a database. When you investigate the database you will often find a users table, which contains usernames and often hashed passwords. It is often necessary to know how to crack hashed passwords to gain authentication to a website(or if you're lucky a hashed password may work for ssh!).

#Salting and Formatting

No matter what tool you use, virtually all of them have the exact same format. A file with the hash(s) in it with each hash being separated by a newline.

Example:

<hash 1>

<hash 2>

<hash 3>



Salts are typically appended onto the hash with a colon and the salt. Files with salted hashes still follow the same convention with each hash being separated by a newline.

Example:

<hash1>:<salt>

<hash2>:<salt>

<hash3>:<salt>


#hashcat 
use :
		hashcat -h

- [ ] What flag sets the mode.

		-m
- [ ] What flag sets the "attack mode"

		-a
- [ ] What is the attack mode number for Brute-force    

		3
- [ ] What is the mode number for SHA3-512    

		17600
- [ ] Crack This Hash:56ab24c15b72a457069c5ea42fcfc640

Type: MD5

		happy
- [ ] Crack this hash:

4bc9ae2b9236c2ad02d81491dcb51d5f

Type: MD4

		nootnoot

# John The Ripper


- [ ] What flag let's you specify which wordlist to use? 

		--wordlist
- [ ]	What flag lets you specify which hash format(Ex: MD5,SHA1 etc.) to use?    

		--format
- [ ] How do you specify which rule to use?

		--rules
- [ ] Crack this hash:

	echo 56ab24c15b72a457069c5ea42fcfc640 > hashfile.txt

	sudo john --show --format=raw-md5 hashfile.txt 
	
	hello 


	echo 5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8 > hashfile.txt

	sudo john --show --format=raw-sha1 hashfile.txt  


	password

