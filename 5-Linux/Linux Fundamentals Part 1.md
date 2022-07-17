# link : https://tryhackme.com/room/linuxfundamentalspart1

Welcome to the first part of the "Linux Fundamentals" room series. You're most likely using a Windows or Mac machine, both are different in visual design and how they operate. Just like Windows, iOS and MacOS, Linux is just another operating system and one of the most popular in the world powering smart cars, android devices, supercomputers, home appliances, enterprise servers, and more.

We'll be covering some of the history behind Linux and then eventually starting your journey of being a Linux-wizard! This room will have you:

Running your very first commands in an interactive Linux machine in your browser
Teaching you some essential commands used to interact with the file system
Introduce you to how users and groups work on Linux (and what this means for us as penetration testers)

If we wanted to output the text "TryHackMe", what would our command be?
	
	echo TryHackMe

What is the username of who you're logged in as on your deployed Linux machine?

	whoami
	tryhackme


On the Linux machine that you deploy, how many folders are there?

	4
	
Which directory contains a file? 

	folder4

What is the contents of this file?
	
	cat filename
	Hello World

Use the cd command to navigate to this file and find out the new current working directory. What is the path?

	cd  /home/tryhackme/folder4

Use grep on "access.log" to find the flag that has a prefix of "THM". What is the flag?

	grep "THM" access.log
	THM{ACCESS}


If we wanted to run a command in the background, what operator would we want to use?
	&
If I wanted to replace the contents of a file named "passwords" with the word "password123", what would my command be?

	echo password123 > passwords

Now if I wanted to add "tryhackme" to this file named "passwords" but also keep "passwords123", what would my command be

	echo tryhackme >> passwords

