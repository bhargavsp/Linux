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


