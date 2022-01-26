
# Introduction to Linux & Terminal commands 

This is something I got while learning Linux with Kunal Kushwaha Devops bootcamp 
Every thing I learnet on the Video You will find here.



## Important Links

 - [Introduction to Linux & Terminal Commands - Full Course for Beginners](https://www.youtube.com/watch?v=iwolPf6kN-k&list=PL9gnSGHSqcnoqBXdMwUTRod4Gi3eac2Ak&index=4)
 - [Complete Devops Playlist](https://www.youtube.com/playlist?list=PL9gnSGHSqcnoqBXdMwUTRod4Gi3eac2Ak)
 - [Github Repo for Codes and notes of Kunal Kushwaha Devops Bootcamp](https://github.com/kunal-kushwaha/DevOps-Bootcamp)


## What is Terminal Emulator
A  terminal emulator is basically a program that will let us use the terminal in a graphical way.  
Using the terminal the User is able to control the operating system   
For example :- Creating a folder we will type command  
```bash
  mkdir folderName
```
## What is Shell
Shell in Linux is command line interface that will take all the commands as input and tell the operating system to do the work
## ls Command
ls command in linux tells the Operating system to list everything available in the current folder/directory.  
current directory/folder is a directory where you are running your command in the terminal.  
```bash
  ls
```
## cd Command
cd stands for Change directory   
You can switch one folder to another folder using cd command  
For example :- assume you are in movies foler and in moves folder there is another folder named EnglishMovies and you want to jump into that folder.  
for this the command is :-
```bash
  cd EnglishMovies
```
by doing this you can move from one folder to another.  
If there is no any folder availabile that you want to open then the command will give you error.  
**Command for Going back from a sub folder to parent folder:-**  
```bash
  cd ..
```
Use .. (double dot) to go back to parent folder.


## Environment Variable
Environment Variable are just named values that are used to change how the commands and processes are executed.  
**Any instance of the running command is called process**

## PATH Environment Variable
PATH  is an environment variable that tells the shell which directories to search the executable file.  

**Command to print PATH Environment Variable**
```bash
  echo $PATH
```

A use case of Environment Variable is :-  
 If we want to store passwords/secrete which we do no want to hardcode in source code we use Environment Variable
## Important Commands To Work with linux terminal
**1. pwd :-** pwd stands for print working directory, it basically display in which directory you are in right now.
```bash
  pwd
```
**2. ls:-** ls stand for list and it display all the contents, file and directory stored in the current directory
```bash
  ls
```
ls command does not show the hidden files and directories available in the current directory  
so to list all files and folder including hidden we use **-a**
```bash
  ls -a
```
-a stand for all

if we want to see properties of file and folder we can use **-l**  
-l displays all the information of files and folder like size of file, permissions of files, owner of files etc.
```bash
  ls -l
```  
  
if we want to see properties of all the file including hidden file we use **-la**
```bash
  ls -la
```   
  
  if we want to see everything inside folder and its all sub folder we van use **-R**
  ```bash
  ls -R
```

**3. cd :-** cd stands for change directory. we can change our directory and change our directory to sub folder of current folder.  
```bash
  cd dirName
```
**dirName can be name of sub folder**  

If we want to go back in the parent folder we can use command  
```bash
  cd ..
```
if we want to change directory from one sub folder to another sub folder having same parent folder we can use command :-  
```bash
  cd../subFolderName
```
**4. cat :-** cat stand for concatinate.  
It is used to list all the contents available in the file as standard output.
```bash
  cat filename
```
It is also used to create a file and write something on that file for this we can use command :-
```bash
  cat > FileName
```
**To come out of the editor which cat opens to write something on the file we use ctrl+c or cmd+c**  

It is also used to merge two files content.  
for example if we want to merge two files content into third file we can do by the command :-  
```bash
  cat file1 file2 > file3
```
above command merge content of two files and put it into third file.

**>** this symbol is used to redirect the output to new file
```bash
  echo "Hello world" > file1.txt
```
the above command override the content of file and put in into file1.txt

**4 man :-** this command is used to display the user manual of any command that we can run on the terminal.
```bash
  man echo
```
**5. tr :-** tr stands for translate it is used to translate the file   
For example :- if we want to translate file1.txt content from lover case to upper case we can use command :-
```bash
  cat file1.txt | tr a-z A-Z > upper.txt

  cat upper.txt
```
**|** this symbol is called pipe   
by using this we can transfer the output of first coomand as input of second command

**6. mkdir :-** This command is used to make directory
```bash
  mkdir parentFolder
```
if we want to create folder inside a folder we can use command :-
```bash
  mkdir parentFolder/hello
```
if we want to create folder in the middle of folder we can use command :-
```bash
  mkdir -p parentFolder/middle/hello
```
the above command create middle folder inside parentFolder  and create hello folder inside that middle folder.  

**7. touch :-** this command is used to create files
```bash
  touch names.txt
```
if we want to create multiple file we can use touch command there also
```bash
  touch file1 file2 file3
```
if we want to create a file inside direcory we can use 
```bash
  touch parent/file.txt
```

**8. cp :-** This command is used to make copy of file 
```bash
  cp file.txt copy_file.txt
```
by above command the content of file.txt will be copied on copy_file.txt

**9. mv :-** by this command we can move out file content from one file to another and this command is also used to rename a file.
```bash
  mv file1.txt newfile1.txt
```
**10. rm :-** this command is used to remove the file or folder permanently 
```bash
  rm newfile1.txt
```
the above command is used to only delete files  

To delete a Folder/directories we can use 
```bash
  rm -R NewFolder

```
Sometime it may happen that file or foler not deleted one of the reason for this is because file is opened.  
So we have to delete the file forcefully.
```bash
  rm -rf newfile.txt
```
**f** stands for forcefully.  
**11. sudo :-** It stands for super user do this command is used to do the task in linux as administrator.
```bash
  sudo echo "Hello World"
```
The above command is used to execute echo commad as administrator.  
**12. df :-** this command is used to check system disk space usage.
```bash
  df
```
the above command is used to show disk space usage in kb.  
So if we want to display disk usage in MB we can use :-
```bash
  df -m
```
**13. du :-** this command is used to display the disk usage by files of current directory.
```bash
  du
```
the above command is not in human redable format.  
So to display the information in human redable format we can use 
```bash
  du -h
```
**-h** sands for human readable.

**14. head :-** head command is used to display first some content of file . By default head shows content of from above 10 lines.

```bash
  head file.txt
```
the above command display first 10 lines of content from file.  
We can explicitly define the lines of content which we want to display as output.
```bash
  head -n 4 file.txt
```
the above command display only first 4 lines of content.  
**15. tail :-** this command is used to display the content of file from last.  
by default it displays last 10 lines of content.  
```bash
  tail file.txt
```
we can explicitly define the lines of content which we want to display as an output.
```bash
  tail -n 2 file.txt
```
the above command display last 2 line of content from the file.  
**16. diff :-** This command is used to display the difference between two files content.  
```bash
  diff fileOne.txt fileTwo.txt
```
The above command display the difference between fileOne.txt and fileTwo.txt. It output those lines which are not different in both files it doesnot show those line which are same in both file.
  
**17. locate :-** This command output the path of the file or we can say locate the file.
```bash
  locate "*.txt"
```
It show the path of files which ended with .txt.  
**18. find :-** This command is used to display everything in directory it also shows hidden files and folder in hierarchical manner.
```bash
  find parent
```
the above command display everything inside parent directory.  

If we want to find only folder in a particular directory we can use.
```bash
  find parent -type d
```
the above command display every folder inside parent directory in hierarchical format.  
So if we want to display ony files not folder we can use 
```bash
  find parent -type f
```
the above command display all the files present in parent folder in hierarchical form.  

To find a particular file we can use 
```bash
  find . -type f -name "two.txt"
```
In above command the file name is case sensitive so if we do not want to be it as case sensitive we can use 
```bash
  find . -type f -iname "two.txt"
```

**19. whoami :-** this command gives output as who is the current user of the system.
```bash
  whoami
```
**20. grep :-** grep stands for global regular expression print.  
It is used to find the text written in a file.  
It is case sensitive.  
```bash
  grep gautam names.txt
```
the above command get the word gautam in the names.txt file and display it as output.
  
  If we want to print athe full word than we can use 
  ```bash
  grep -w "gautam" names.txt
```
As we know it is case sensitive this does not show the word if we do not write the same word in same way
  
  so if we want this command to act as not case sensitive we can use :-
  ```bash
  grep -i "gautam" names.txt
```
we can combine two comman also like :-
```bash
  grep -iw "gautam" names.txt 
```
the above command gives full word and does not act as case sensitive also.
  
  If we want to print the text with line number we can use :-
  ```bash
  grep -n "gautam" names.txt
```
  
  But here we know that gautam is written in names.txt but what if we dont know that.  
  then we can search in a directories like :-
  ```bash
  grep -win "gautam" ./*txt
```
  
now there may be a condition we don't know in which sub directory the gautam text is present so we can use :-
```bash
  grep -rwin "gautam" .
```
the above command search gautam in the current folder recursively means it will find in each and every directory of parent folder.
  
  Now if we want to display all the files that contain gautam we can use 
  ```bash
  grep -wirl "gautam" .
```
the above command display all the files that contain gautam text in it.  

we can also count how many files and with faile conatin how many times gautam text.
```bash
  grep -wirc "gautam" .
```
**21. history :-** This command is used for displaying all the Commands you used.
```bash
  history
```
if we want to get history of only ls command we can use grep command with it using pipe (|)
```bash
  history | grep "ls"
```
the above command display only history of ls command.  
  
**22. top :-** this command is used to display the cpu usage, memory usage and other stuffs of the active applications that are running. 
  ```bash
  top
```
**23. hostname :-** this command gives the name of system or DNS name of the system.
  ```bash
  hostname
```
to get ip address of hostname or system we can use **-i** tag  
  ```bash
  hostname -i
```
above commad gives the ip address of host.  
There are so many tags available with hostname to get information about system.
**24. free :-** this command is used to check the free and used memeory of system.
  ```bash
  free
```
the above command gives memory details in kb .  
  ```bash
  free -h
```
he above command gives memory details in GB.
**25. vmstat :-** this command is used to display the virtual mmemory details.
  ```bash
  vmstat
```
**26. lsof :-** lsof is used to display the information of files which is opened by any of the process of computer.
  ```bash
  lsof
```
**we can also list all the file that are opened by particular user**
  ```bash
  lsof -u Username
```
the above command display information of file that are opened by Username.  
  
    
**27. cut :-** this command is used to cut out the selecter portion of each line of a particular file
  ```bash
  cut -c 1-2 names.txt
```
the above command gives output as only 2 words from each line from file names.txt
## File Permissions
When we talk about files we always talk about permission also.  
And there are three types of people who is using Your computer  
1. User :- user can be any person or an account on a computer or else
2. Group :- group is like a particular entinty foer example for a particular user there can be multiple group like sudo group.
3. Other :- Other stands for other people except the above two.  
  



r = read permission  
w = write permission  
x = execute permission  
To see the permissions of a particular file we can use :-
```bash
  ls -l upper.txt
```



above command shows the meta data of upper.txt file.  
We can change the permisssion of file using two ways with chmod command:-  
**i) Alphanumeric mode :-**   
let say we want to change the permission of upper.txt we can use command :-
```bash
  chmod u=rwx,g=rx,o=r upper.txt
```
above command change the user permission of upper.txt to   
user has read, write and execute permission.  
group has read and execute permission.  
others has only read permission.  
  
  to check the permission of upper.txt we can again use 
  ```bash
  ls -l upper.txt
```
**ii) Octal number :-**   
In octal mode   
read has value 4  
write has value 2  
execute has value 1  
for no permission  0 is used 
  
  If we want to change the permission for user group or other we can add the number of permission and assign them to user, group or other.  
    
**for example :-**  
we want to change the permission of user to read write and execute and group to read and execute and other has no permission   

so we can calucalte it as 
user - rwx = 4+2+1 = 7
group - rx = 4+0+1 = 5
others - no permission = 0+0+0 = 0  
  
  so we can change the user permission of file1.txt as :-
  ```bash
  chmod 750 file1.txt
```
  
  If we want to find the files who has some permission.  
  for example find the file who has permission of 777 we can do this by command 
  ```bash
  find parent -perm 777
```
the above command is used to find the files who has permission 777.
## Change Owner of file
As we can change the permission of file we can also change the owner of file.  
But to change the owner we must have root access   
   
   to get root access we can use 
   ```bash
  sudo
```

**To Change the owner of the file we can use**
```bash
  sudo chown file2.txt
```
The above command change the owner of file to root.  


**what is root?**  
  
  root is the super user account in the linux base system.   
  it is bascically used for admistrator purpose.   
  root has most highest number of access rights in the system.
## alias in linux
alias command instructs the shell to replace one string with another string while executing the commands.   
When we often have to use a single big command multiple times, in those cases, we create something called as alias for that command. Alias is like a shortcut command which will have same functionality as if we are writing the whole command.   
  
  to create alias we can use :-
  ```bash
  alias name="value"
```
here value can be any command.
for example :-  
  ```bash
  alias CD= "cd Desktop"
```
above command create alias for changing directory to Desktop.

**How to remove alias?**
Removing an existing alias is known as unaliasing.  
to remove and alias we can use :-
  ```bash
  unalias [alias name]
```
for example we can remove CD alias
  ```bash
  unalias CD
```
the above command remove CD alias.  
  
  To list all the alias we can use :-
  ```bash
  alias -p
```
**How to permanently store aliases across sessions?**
We can store aliases in shell configuration files.   
For example for Bash Shell, we can write in ~/.bashrc.   
and for zeeshell we can use ~/.zprofile

## Download anything from internet
For downloding anything from the internet we can use wget command
  ```bash
  wget URL
```
URL Can be a web link which is used to download the stuff from internet.  
  
**How to save the downloded file with any name?**  
for this we can use **-o** :-  
  ```bash
  wget -o URL
```

## zip and unzip files
using zip command we can zip files.  
zipped foler has extension .zip  
for example :-  
I want to zip a file named myfile.txt so I run the command 
  ```bash
  zip zipfile myfile.txt
```
the above command create a zip folder with myfile.txt file in it. 
  
  **We can zip more than one file**  
```bash
  zip morefile file1.txt file2.txt file3.txt file4.txt
```
the above command create a zipped folder of named morefile and file1.txt, file2.txt, file3.txt, file4.txt will be in it.


**How to unzip the zipped folder?**  
for unzipping a folder we can use :-  
  ```bash
  unzip morefile.zip
```
the above command unzip the morefile.zip folder.

## Adding and deleting users
To add new user we can use command 
  ```bash
  useradd Username
```
User name can be any name we want to give.  
To set the password for user we can use command :-
  ```bash
  passwd Username
```
the above cammand asks the password and set for the user.
  
    
**How to delete user ?**  
To delete user we can use command :- 
  ```bash
  userdel Username
```
Username can be any name of user which is already exist on the computer.  
  
**we can ckeck if any particular user exists or not**
  ```bash
  getent group Username
```
the above command tells us if user exist or not if exist the terminal display Username with its id.  
**we can also display the id of user**
  ```bash
  id Username
``` 
the above command is used to get the id of user.
## uname command
uname command is used for various usage :-
  ```bash
  uname
```
the above command gives the name of kernal
  ```bash
  uname -o
```
the above command gives the type of linux kernal
  ```bash
  uname -m
```
the above command is used to get the architecture of the linux.
  ```bash
  uname -r
```
above command is used to get the version of kernal.

## Information about Operating system
If we want to get all the information related to operating system we can use :-
  ```bash
  cat /etc/os-release
```
We can also get the Details of CPU by command :-
  ```bash
  lscpu
```

## Networking Commands
To check the ip address of any domain we can use 
  ```bash
  nslookup google.com
```
the above command is used to check the ip address of google.com domain.  
  
    
To check all the active ports we can use :-
  ```bash
  netstat
```

## Working with Operator
We can work with operators in linux command line.  
by the help of operators we can combine various commands.  
  
1. **And operator (&) :-** this operator is used to run a command in the background so that other command can be executed.  
It is also known as child process creation.
  ```bash
  ping google.com & ping commclassroom.com
``` 
2. **And And operator (&&) :-** this command is used when we want that the command that is succeding the operator will only execute when previous one is finished execution.
  ```bash
  echo "first" && echo "second"
```
3. **Semicolon Operator (;) :-** this command is used to put two or more commands on the same line separated by the semicolon. All the arguments before (;) will be treated as a separate command from all the arguments after the (;).  
  ```bash
  touch file1.txt; cd Desktop; touch fileonDesktop.txt
```
4. **Or operator (||) :-** the command after the or operator will only execute if the command before the operator will fail or not executed.  
  ```bash
  echo "first" || echo "second"
```
in above command only first will display because the first command is executed so command after or operator does not execute.
  ```bash
    vasbkxsabj && echo "second"
```
In above command second will displayed on the screen because the command before or operator is invalid so it does not executed so echo second will execute.  
  
5. **pipe operator (|) :-** this operator sends the output of one command as input of second command.
  ```bash
   history | grep "ls"
```
the above command display only history of ls command.  
6. **not operator (!) :-** Logical not (!) is boolean operator, which is used to test whether expression is true or not. For example, if file not exists, then display an error on screen. 
or  
it can be used for deleting all file except a particular file.   
  ```bash
   rm -rf !(token.txt)
``` 
7. **>> :-** this is used for append something on a file for example :-
  ```bash
   echo "hey" >> names.txt
``` 
8. **> :-** this is used for override the content of file.
  ```bash
   echo "hello" > names.txt
``` 
above command override the content of file now names.txt file contain only hello.  
9. **combination operator ({ }) :-** this operator is used to combine two or more commands 
  ```bash
   echo "hey" && {echo "hi"; echo "i am good"}
``` 
echo "hi" And echo "i am good is now combined"
