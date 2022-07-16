- [ ] First, you have to use search the directory with “gobuster” : 

		gobuster dir  -u http://10.10.109.43/ -w /usr/share/dirb/wordlists/common.txt  -t 64 -q
		

![f1](https://user-images.githubusercontent.com/94765997/179359676-0829bed4-3244-4ea2-a500-9a45a606c2a5.png)

- [ ] second search in /secret : 

		gobuster dir  -u http://10.10.109.43/secret/ -w /usr/share/dirb/wordlists/common.txt -x .txt -t 64 -q
		

![f12](https://user-images.githubusercontent.com/94765997/179359688-778f375f-6bdc-45f4-804d-cb2b2a206aba.png)

- [ ] we find secret.txt : 

![f3](https://user-images.githubusercontent.com/94765997/179359696-f960527f-c268-4659-8807-57f8e7c8d1b9.png)


- [ ] crack the hash and get ssh key :

![f2](https://user-images.githubusercontent.com/94765997/179359701-030712c8-dd7c-4bf8-bd41-0fbee1fddc45.png)


- [ ] connect to ssh and get flags  : 

![f5](https://user-images.githubusercontent.com/94765997/179359713-bbd5957e-4ecd-4b4c-a690-614f281a1f6c.png)


