- [ ] First, you have to use search the directory with “gobuster” : 

		gobuster dir  -u http://10.10.109.43/ -w /usr/share/dirb/wordlists/common.txt  -t 64 -q

- [ ] second search in /secret : 

		gobuster dir  -u http://10.10.109.43/secret/ -w /usr/share/dirb/wordlists/common.txt -x .txt -t 64 -q

we find secret.txt : 


crack the hash and get ssh key :


connect to ssh and get flags  : 

