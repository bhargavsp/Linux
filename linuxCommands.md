## Linux Commands

| Command | Usage | Example Command |
| :-----:   | :-----: | :-----: |
|  **`ssh`**    | it is used to ssh into the server (secure shell) |  |
| **`chmod`**   | used to ***Give*** or ***Change*** the permissions of a file or a folder |  |

### File mangement commands
 
| Command | Usage | Example command |
| :---: | :---: | :---: |
| **`cd`** | takes to the Home directory | cd |
| cd .. | go one step to the previosu directory | cd .. |
| cd ~ | go to the *Home Direcotry* | cd ~ |
| cd - | It takes to the previous directory (something like back in the chrome) | cd - |
| **`mkdir`** | It is used to create a directory in linux |  |
| mkdir -v | gives the ***information*** in next line of what the command execute | |
| mkdir -p | creating ***multiple Directories*** at the same time | mkdir -p devops/linux/shell/git | 
| mkdir -m | creating the folders/directories with some custom permissions | mkdir -m 700 devops |
| **`touch`** | used to create a file in a particular folder | touch devops.txt |
| **`ls`** | list the files and folders in a particular path | ls |
| ls -l | list the long listing of the files and folders in a paticular folder | ls -l|
| ls -ltra | list the files/folders in a ***long listing, time stamped, reverse order and all files*** | ls -ltr | 
| ls -li | It is used to display the Inode number for the file/folder | ls -li |
| ls -lh | display the files/folders in the human redable formats
| **`Find`** | it is used to search the file by using variety of conditions like *permissions, users, groups, file type, data, size* | | 
| find . -type f -empty | . is from the particular directory | |
| find / -type d -empty | / is the complete file system but it works only at root user level, we cannot access entire file system as a normal user | |
| find . -iname | *i* option is used to ignore the case sensitive and search | find . -iname Mithun.txt | 
| umask | user mask value is fixed value given to root or normal user to create a file or directory, so only the specified permissions are given to the files/direcotries while the particular user is creating | |
| **`chmod`** | used to change the permissions of the file | chmod 777 devops.txt |
| **`chown`** | used to change the owner permissions of the file | chown root devops.txt |
| **`chgrp`** | used to change the group permissions of a file/directory | chgrp ec2-user devops.txt |
| chgrp -R | To change the group name of the file/folders *RECURSIVELY* means changing all the group of the files/directories | chgrp -R ec2-user devops.txt |
| **`cp filename/direname targetdir`** | To copy the files/directory form one dir to another directory | cp devops.txt jenkins/ |
| cp *.txt jenkins/ | copy all the .txt files from current dir to jenkins dir | |
| **`mv oldfilename newfilename`** | rename the file name | mv test.txt mss.txt | 
| **`file`** | check and let us know what type of content is there in the file, it is used to check what type of file for the user | file devops.txt | 
| **`WC`** | word count it tells how many lines, words, characters are there in a file | wc devops.txt | 
| **`ln`** | its a link we have hard link and soft link in this |  
| Hard link --> ln oriFile linkFile | only for files we can create hard link, same permissions for both files, inode number is same | ln devops.log backup.log
| soft link --> ln -s oriFile linkFile| files/dir we can create soft link, each file has there own permissions, inode number is diff | ln -s devops.log backup.log

### Text reading/ display commands

| Command | Usage | Example command |
| :---: | :---: | :---: |
| **`se nu`** | to display the line numbers in the file when opened in vi editor in command mode | :se nu |
| se nonu | not to display the line numbers in the file | :se nonu |
| /text | find the text in the file in vi editor in command mode | /hello |
| echo | Used to print the output | echo hello |
| cat -n | display the line numbers next to the lines in file | cat -n devops.txt |
| head filename | prints first 10 lines | |
| head -15 filename | prints first 15 lines | |
| head -n 15 filename | prints first 15 lines with number next to it | |
| tail -f filename | also print the last updated 10 lines | | 
| **`more`** | displays the lines in file in forward/backward direction one screen at a time | more devops.txt | 
| **`less`** | display the lines in file in forward/backward direction line-by-line | less devops.txt |
| **`sort -r`** | sort by alphabetical order in reverse | sort -r devops.txt |
| tr [a-z] [A-Z] | transcalting lower to upper case all letters in file | tr | 
| sed -n | print content from the file sed(stream editor) means output going to update not update the whole original file | sed -n "86,90p" devops.txt |
| sed "s/red/blue" devops.txt | prints the output with replaced content of first occourance red to blue word | |
| sed "s/red/blue/g" devops.txt | prints the output with replaced content globally changes in file from red to blue word | |
| sed -i "s/red/blue" devops.txt | edits the whole original file also | |
| grep | which stands for *global regular expression print* , processes text lineby line and prints all the lines matches specified pattern | |
| grep -i "command line" /etc/ssh/ssh_config | it searches the file for hte matches text inside the quotes | |
| grep  -R text directory | searches the text in the file recrusevely for the text to match from the whole directory | grep -R hello /etc |
| wc -l| word count | |
| locate | used to locate the file same as search in windows, first install the locate and use -i to serch regardless of the case | locate -i devops.log |
| diff | find the difference b/w 2 files | diff text.txt text1.txt |

### User/Group administration Commands

| Command | Usage | Example command |
| :---: | :---: | :---: |
| **`sudo su -`** | Used to switch to the ***root user*** in linux | sudo su - |
| useradd usernmae | to create an user in linux | useradd bob |
| passwd username | to set the password for the username that is created | passwd bob | 
| chage username | it is used to set the attributes to the user such as set the limits for the user like mim pass, mac pass, last pass change, pass expir, pass inactive, account expiration data | chage bob |
| groupadd grpname | to create a group | groupadd devopsteam |
| usermod -g username | used to add the users to the groups | usermod -g devopteam bob |
| usermod -aG | to set the primary and seconday usergroups | usermod -aG devopsteam bob |
| lid -g groupname | list the users in the particular group | lid -g devopsteam |
| id username | prints the UID, gID, secondary gid | id bob |
| su username | su means switch user | su bob | 
| userdel -r username | to delete the user from server | userdel -r bob | 
| groupdel groupname | to delete group from the server | groupdel groupname |

### communication commands

| command | Usage | Example command |
| :---: | :---: | :---: |
| wall "message" | brodcast the message from the root user to rest of all the users in the server | wall "message restart in 10min" |
| write "message" | communicate from user to another user in the server | wall "I am uodating the cleanup file" |
| mesg n | to disable the messages from other users to me | mesg n |
| mesg y |  to enable the messages from other users to me | mesg y |
| mail | to send and reads the email from server we use SMTP server and pop, pop3 servers | 

### stream editor commands
| command | Usage | Example command |
| :---: | :---: | :---: |
| cut -d | -d means delemeter means separator of 2 statements, here f2 is the field2 | cut -d "=" -f2 | 


### additional commands
| command | Usage | Example command |
| :---: | :---: | :---: |
| cal -3 | displays the past 3 months of the current calendar month | cal -3 |
| cal 2024 | displays entire calendar of 2024 | | 
| cal Apr 2020 | displays the apr month of the 2020 year | |
| wget url | to download the 3rd paty softwares into the server | wget url |
| curl -o outputfilename url | same as wget need to display the output file name and give the URL | | 
| tee | display the output of the other command to the consile and also redirect to the other file, it does both the jobs | ls | tee teeopt.log |
| script | it is used to record the list of the commands and the outputs everything and save it to the *typescript* named file (it is simillar to the screenshot in the windows, captures everything) till we enter the exit commands to stop the script | script|
| script -a bob.txt | instead of the typescript file name we are specifying our own filename to save the script after we give the *exit* command, -a option appends the script to the same bob file | |


### Remote access commands

| command | Usage | Example command |
| :---: | :---: | :---: |
| ssh username@ipaddress/hostname | used to ssh into the server using the public ip address or the hostname | ssh ec2-user@54.158.243.186 |
|scp | copy files from one server to another server using secure copy | scp filename username@serverip/hostname:path |

### Installing/Config commands

| Command | Usage | Example command |
| :---: | :---: | :---: |
| **`yum install`** | Install packages in the ***redhat/centOs*** | yum install tree |
| **`yum install -y`** | Install packages in the ***Interactive mode in redhat/centOs*** | yum install tree -y|
| netstat -r | dispplays the route table | |

### what are attributes in linux

### system resources commands

| Command | Usage | Example command |
| :---: | :---: | :---: |
| who | displays information about all users currently on the local system | |
| who -H | *H option* displays the heading of the columns displayed | |
| w | it gives the complete information of the server up-time, user logged in, load for 1, 5, 15min on the server, commands excited by each user etc...
| uptime | It displays the uptime of the server | uptime |
| users | dislays the list of currently logged in at this time | |
| stress | It give the stress incresases load at the 8 cores to the system | stres -c 8 --timeout 10|
| whereis | path/locate the binary, source and manual page files for a command | whereis ls|
| whatis | give the small info of a commans | whatis ls |
| date | we can display the timezone and time of the server and also set it | date -s "20240509" |
| timedatectl | control and set the timezone and date | |
| df | know external devices connected and the size of the harddisk | df -h |
| du | it estimates and shows the file space usage | du -s jenkins/ |
| hostname name| gives the hostname of the server and aslo can change the srever name | hostname bhargav.com |
| hostname -i | displays the public IP of the server | |
| ifconfig/ip a | gives the IP address and some info about the server | |
| systemctl list-unit-files | list all the services are running in the linux | |
| service servicename options| check the service and start/stop etc... | |
| systemctl options servicename | check the service and start/stop etc... | |
| last | gives the list of last logged in user in the particular server | |
| visudo | safely edit the sudoers file | visudo |

### Hardware related commands

| command | usage | Example command |
| :---: | :---: | :---: |
| free -h | check the ram consumption in human readable format | |
| dmidecode | it gives the whole ram and hardware information and type of hardisk used for the server | |

### process management commands

| Command | Usage | Example command |
| :---: | :---: | :---: |
| ps | gives the process that are running for current user  | |
| ps -ef | gives the processes of all the users in the server | |
| pidos processname | gives the process if of the particular service | pidof bash |
| kill | kills the process or signals the process with the signal type/code | kill -9 apache2 |
| top | displays all the system resources utilization (cpu, ram etc...) | top |


### Autoamting/scheduling Tasks commands

| Command | Usage | Example command |
| :---: | :---: | :---: |
| crontab -ler | displays the list of crontabs, or edit or delete that are scheduled in the server |  |
| https://crontab-generator.org/ | website for the crontab generation | |
| yum install cronie -y| used to install the crontab package| |

![image](https://github.com/bhargavsp/Linux/assets/45779321/bb789f3b-3f19-4bcf-83c1-3a7dcb9b61aa)


### Archive/Data Backup commands

| Command | Usage | Example command |
| :---: | :---: | :---: |
| zip -r | zipping the foler | Zip -r abc.zip devops |
| unzip | unzip the archive folder | unzip devops.zip | 
| tar -cvf newfilename sourcefile | tar create, verbose, filesystem the folder | tar -cvf abc.tar devops |
| tar -xvf filename | tar extract, verbose, filesystem | tar -xvf devops.tar | 






Addtional Material:
![image](https://github.com/bhargavsp/Linux/assets/45779321/ae0a23dd-b4e9-4067-9b36-715e905e4950)


