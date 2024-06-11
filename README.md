# Linux

## SSH Tools

These are used to login into the instances or SSH into the server

### Putty
### SUperPutty
### Mobaxterm
### Gitbash

For *Mac* we have **Terminal (Default SSH)**
For *Windows* we have **Power Terminal (command Prompt, Powershell, WSL(Windows sub system for the Linux))**


Linux is a multi-user, multitasking Operating System, Open source and it is mainly Case-sensitive(uses the lower case for most of the commands)
Language used to develop the *Linux OS is C*

**Linux flavours with the distributions**

Redhat
centOS
Ubuntu
SuSe Linux 
Fedora etc.....


## LINUX File STRUCTURE


**/ is rootDirectory/parentDirectory in Linux**

Folder --> is called the Directory in the Linux/Mac

**home**
It is the home directory, we have all the users created for the particular server

**bin**
We have all the binary files for the commands that we use in the linux

**sbin**
secure bin, only the root user can access the folder and binary files in it

**etc**
contains all the config files. only root users can access these files but some files the normal users can read it but cannot update it 
*EX:* passwd, shadow, group, sudoers

**dev**
Devices that are connected to the particular server can be seen here 

**Proc**
for every task we execute in the linux there will be a process ID created, here all the process ID's are created
cpuinfo file: cores of CPU, architecture everything about the current CPU

**Lib**
files available in lib dir can only be used by the operating system

**temp**
temperory files that we can create and delete after sometime, those files can be stored here, these folder can be accesses by all the users

**Var**
all the logs can be seen here, and the system users home directory can be seen here

**opt**
By default it is empty directory, all the 3rd party softwares can be installed here, it can be accessed only by root user.



### Types of users in the LINUX OS

root user/ super user/ admin user
normal user: root user creates normal users and each user have there own home 
System user: system users are automatically created when installing the softwares
*EX*: Apache HTTP server --> apache user --> one of the system user 



