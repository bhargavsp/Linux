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
| sed -n | print content from the file | sed -n "86,90p" sudoers |


### User Commands

| Command | Usage | Example command |
| :---: | :---: | :---: |
| **`sudo su -`** | Used to switch to the ***root user*** in linux | sudo su - |

### Installing/Config commands

| Command | Usage | Example command |
| :---: | :---: | :---: |
| **`yum install`** | Install packages in the ***redhat/centOs*** | yum install tree |
| **`yum install -y`** | Install packages in the ***Interactive mode in redhat/centOs*** | yum install tree -y|

Addtional Material:
![image](https://github.com/bhargavsp/Linux/assets/45779321/ae0a23dd-b4e9-4067-9b36-715e905e4950)


