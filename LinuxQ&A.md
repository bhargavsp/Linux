### **What if we want to login into the server and upload and download the files from the server to the local computer?**
We have to use the *FTP tools* to securely login into the server and upload and download the files to local computer
*For Windows* --> WinSCP (Windows secure Copy)
*For Mac* --> Filezilla (It works in the Windows/Mac/Linux) and Cyberduck

### Difference between bin and sbin?
Binary files in *bin* directory can be accessed by *all the users* including the system users
Binary files in *sbin* directory can be accessed only by only *root user*


***Learn the Linux file system*** 


***There should be no spaces in the AWS Key pair***


### what happens if we give the space in b/w the names while creating the files and folders?
It Linux the space is considered as the separator and creates 2 files/folders instead of one single file name

### what if key pair is lost for the server in aws, can we login into that or not?
There is a No way logging into the server but we can take the backup of the entire server and restore it into an another server.

### how to check whether we connected to linux server or not?
we can use the *uname* command and if the output is Linux, then we can say that we connected to the linux server

### How to create a directory with some custom permissions?
if we create an directory using the mode while creating we can give the custom permissions
*Ex:* mkdir -m 700 devops 

### how to install the packages in linux without interactive mode(means without asking yes or no while installing the packages/softwares in linux)?
We have to use the ***-y*** option while executing the linux command
*Ex:* yum install tree -y

### Difference between *sudo su* and *sudo su -*?
***"su"*** gives you root powers, but keeps your current user environment and home diretory and current user configurations
***"su -"*** switchs to the root user and home dir environment, root user configurations, root home directory---just as if you had logged in as root.


### How to know the directories and files in the linux file system? 
ls -l and there if the file permissions ***starts with the d then its directory*** else if it ***starts with - it is a file***
*Ex:* drwxr --> directory, -rwxr --> file

### what is *-ltr* options in the *ls* command
*l means long listing*
*t means time stamped*
*r means reverse order*

### How to create a folder/file hidden in linux
using the ***. (dot)*** before the file/folder name while creating

### what is Inode in linux?
Inode is a data structure, It can be used to store the *file/dir Info* except the file or directory name. Basically it is the Unique number, These file and folder names are for the user use, linux uses the Inode to remember and access the file and folder 

### what is the format of file size in the linux?
By default all the files and folders size is shown in the bytes

### how to search all the empty files in the current directory?
By using the *find* command ***find . -type f -empty***  

### how to search all the empty directories in the current directory?
By using the *find* command ***find . -type d -empty***  

### what is root user home dir?
It is */root* not the / or /home/root

### default permissions of the file and directory?
for *file 666*
for *directory 777*

### default umask permissions for the users root or normal user?
It is *022* the default permissions

### how to change the files/dir owner and group permissions with a single command?
yes we can change with the ***chown ec2-user:ec2-user devops.txt***

### why do we use link?
lets take a use-case scenario --> after deploying a application we get logs, and those cannot be accessed by the devloper because those were stored in the /var/logs/apache.log folder which cannot be accesed by normal user except the root user, so to access the logs we create a soft link and store the file in the temp/ directory 
