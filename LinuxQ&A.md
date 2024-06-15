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

### diff between tar and zip?
tar archieve comppress to veyr less size than the zip

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

### how to make the terminal/ SSH connection acive for long time?
create an *config file* in local laptop
vi ~/.ssh/config
![image](https://github.com/bhargavsp/Linux/assets/45779321/2852a047-6485-4282-84c2-cbd8dbdc1940)

### Nano editor commands
ctrl+o --> saving
ctrl+x --> close

### how to say cpu is 100% utilized in server
type *w* command in linux if the load average is more than 1.0 then the cpu is 100% utilized in general

### realtime scenario --> if the server load average is 6.9 still the cpu is not 100% why?
the cpu utilization is based on the no. of cores cpu
*ex:* if it 8 core CPU, 6.9 load is very less and cpu is not 100% utilized

### what happens if we change the hostname of the server?
if we type hostname -i it displays the host ip address of the linked new hostname
*EX:* hostname google.com

### how to know all the users in the server?
cat /etc/passwd or ls -l /home as every normal user have the /home directory created automatically

### what happens if we create a user in linux
it creates an entry in /etc/shadow or passwd or group

### explain the cat /etc/passwd | grep bob output and the output *bob:x:1001:1001::/home/bob:/bin/bash*
gives the list of users in server and fetches the bob user.
1001 --> UID (userID)

### where the password is stored for the created users in linux?
in the /etc/shadow file

### How to add users to the group
we use the *usermod -g groupname username*

### how to know which group contains how many users/
lid -g groupname

### what are primary and secondary groups in the linux?
primary 
secondary

### how to know the user is locked in linux?
go to /etc/shadow and check if there is an ***! mark *** next to the password it meant the user is locked
use *usermod -U username* to unlock the user

### How the user switching works password requirement in the linux?
su --> switch user
NU --> NU --> password is required
NU --> root --> password is required
Root --> NU --> password not required

### how to provide the admin access/sudo priviliges for the normal users?
we add the user to the /etc/sudoers file to give the admin access to the normal user

### what is visudo command in linux?
To edit and lock the particular, with not being giving access to the other users to edit/update the file

### when the swap memory is used in linux and also from where we get the swap memory is it an extra ram?
The swap memory is used when the 100% of the ram is utilized for the ram and it the swap memory is created by using our hardisk memory. swap memory standard size is basically double the ram we have for the server

### how to change or use the normal user instead of default ec2-user to connect to the ec2 instance?
Fistly, we should login ino the ec2-user and then modify the ***passwordauthentication yes*** in the /etc/ssh/sshd_config file, so then we can login into the server with the other user credentials apart from the default ec2-user

### how to disable the crontab access for all the users expect the root user in server/
1. create a file called *cron.allow* in /etc/. The server automatically detects the creation of the file and disables the access of crontabs to the users. we can add the user name to the cron.allow to give access to the particular user

### setup the crontab
To setup the crontab we should first 
1. install the cronie (yum install cronie -) the crontab package
2. check the *crond.service* service is running or not by using commands *service crond.service status* if not active it
3. create the cronjob for the file ***/1 * * * * /home/ec2-user/hello.sh >> /home/ec2-user/hello.log 2>&1**
4. we are creating the cron job and gave the hello.sh file and redirected the output to hello.log file, and also specified what kind of output need to be saved in the log file i.e 2>&1 (means output and error)
5. file descriptors : 0 --> std input; 1 --> std output; 2 --> std error

## dif between curl and wget
Curl supports multiple protocols like ***restAPI, github api, nexus api***

### how to display output to the console and also redirect to the different command?
use the tee command
*Ex:* ls | tee teeopt.log



