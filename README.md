# Linux

## Best reference for the LINUX and SHELL SCRIPTING
https://web.stanford.edu/class/cs45/
https://linux-kernel-labs.github.io/refs/heads/master/lectures/intro.html#typical-operating-system-architecture

### Typical Linux Operating system architecture
![image](https://github.com/bhargavsp/Linux/assets/45779321/9c779091-ec91-4fc9-a4d3-50e9368d0ec0)


### Linux file system
https://www.thegeekstuff.com/2010/09/linux-file-system-structure/#google_vignette

## SSH Tools

These are used to login into the instances or SSH into the server

### Putty
### SUperPutty
### Mobaxterm
### Gitbash

For *Mac* we have **Terminal (Default SSH)**
For *Windows* we have **Power Terminal (command Prompt, Powershell, WSL(Windows sub system for the Linux))**


***Linux is a Less cost, open source, multi-user, multitasking Operating System, Open source and it is mainly Case-sensitive(uses the lower case for most of the commands)
Language used to develop the *Linux OS is C****

**Linux flavours with the distributions**

Redhat
centOS
Ubuntu
SuSe Linux 
Fedora etc.....
check this websie for more linux distributions https://distrowatch.com/dwres.php?resource=popularity

### USER SPACE VS KERNAL SPACE
The key difference between user space and kernel space lies in their levels of access and privilege within a computer system. The kernel space is privileged and has unrestricted access to system resources, managing tasks like device drivers and memory management, while the user space is where regular programs and applications run, with restricted access to system functions.

So, in simple terms,

User Space: This is where your applications live. Each application gets its own private area of memory to work in, and they’re not allowed to mess with each other’s spaces or the kernel space. It’s like each application has its own private office to work in.

Kernel Space: This is the operating system’s private area. The kernel is the core of the operating system, and it needs its own space to manage the system and interact with the hardware. It’s like the control room of a building, where all the important decisions are made.


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

![image](https://github.com/bhargavsp/Linux/assets/45779321/f4e465f4-b32b-4549-b2f4-17a81afb3893)


### Types of users in the LINUX OS

root user/ super user/ admin user
normal user: root user creates normal users and each user have there own home 
System user: system users are automatically created when installing the softwares
*EX*: Apache HTTP server --> apache user --> one of the system user 


### Crontab:





### Some more linux commands
 ![image](https://github.com/bhargavsp/Linux/assets/45779321/fd7b1d53-0036-4a56-bc0d-190380d508bd)


