using sudo su root to change my shell into a root shell and the prompt asked me to enter the hosts password before changing the shell
![alt text](image.png)
Next would be viewing the difference between useradd and adduser
useradd just creates the user and does nothing else. while adduser creates a group the user and sets them up to the home directory.

Next I will change my user to sally using sudo su sally and it should change from kevin to sally.
![alt text](image-1.png)

I attempted to create a user with sally to ensure she didn't have any sudo privallegs and it turned to be true she didn't have the perm to certe a user.
![alt text](image-2.png)


I exited the root as it not wise to practice doing things in root as it can lead to someone easliy changing files or breaking things if I leave the root shell open when I'm not near
I'm just going to view the ID of my user using id
![alt text](image-3.png)

Ubuntu by default belongs to several groups
![alt text](image-4.png)
I updated sally's permission so they could also execute sudo commands using sudo usermod -aG sudo sally
![alt text](image-5.png)
I created a new user enusring sally permissons upgraded
![alt text](image-6.png)
Next I created a group named cybersec using "sudo groupadd cybersec" then added sally to the group using getent group cybersec
![alt text](image-7.png)
![alt text](image-8.png)

I created a new directory using mkdir and created a section where I can hold code I will refer to as labs
I checked the permissons of this directotry using ls -la lab1 and it showcases my user as both the owner and group owner both eligible to read write and execute 
![alt text](image-11.png)

I made a executable file using nano text editor just to print hello world using echo
![alt text](image-9.png)
as well as in c
![alt text](image-10.png)

Next I messed with file permissions primarily with the group using chmod g=rwx and rw for helloWorld
![alt text](image-12.png)

Using getfacl I just view the ACL of the file
![alt text](image-13.png)

Next I will give someone else permisson to access to a user to write to my file without being in the group or owner
![alt text](image-14.png)
Sally was succesfully given permison to alter my file
using the setfacl command "setfacl -m u:sally:rw- helloWorld" I didn't need to use sudo for any files in lab1 since it is owned by me and not root.
