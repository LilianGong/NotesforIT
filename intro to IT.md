## Basic Command Lines for LINUX

* #### list directory<br>
ls / *show files in the root directory*<br>
ls ~/workspace<br>
ls -l ~/workspace *list detailed 
information*<br>
ls -l -a ~/workspace *list all files including hidden files*<br>
* #### change directories <br>
cd /users/lilian *use absolute directory*<br>
cd ~/lilian *use relative directory*<br>
* #### creat folder<br>
mkdir my-first-folder<br>
mkdir my\ first\ folder *use backslash to interprete the space* <br> 
* #### creat file<br>
touch my_first_file.txt <br>
* #### check the input line history<br>
history *show all past history*<br>
ctrl+R *search for certain history*<br>
clear *remove all input history* <br>
* #### copy files and directories<br>
cp *.png ~/lilian *copy all png files into ~/lilian* <br>
cp -r my_file ~/lilian *copy my_file and all subject directories and files into ~/lilian*  <br>
* #### move and rename files and directories<br>
mv ~/yellow.txt ~/blue.txt *rename file without moving*<br>
mv ~/yellow.txt ~/lilian *move file without renaming*<br>

* #### remove files and directories<br>
rm ~/yellow.txt *remove a file*<br>
rm -r ~/my_file *remove a directory*<br>
rmdir ~/my_file *remove a empty directory* <br>

* #### display file contents<br>
cat ~/yellow.txt  *display the whole file*<br> 
less ~/large_file.txt *display the first page, and use enter /down to go by lines, use tab to go by pages, q to quit, g to the first line, G to the end of the file, and /word_search to search for certain words/phrases* <br> 
head large_file.txt *head 10 lines in the file* <br>
tail large_file.txt *tail 10 lines in the file* <br>


* #### search within files<br>
grep import *.py *search 'import' in all python files* <br>

* #### I/O redirect <br>
echo woof > dogs.txt *put a word in  a file that overwrite the previous contents*<br>
echo woof >> dogs.txt *put a word in  a file without overwriting the previous contents*<br>
ls ~/non_exist.txt 2> /dev/null *output the standard error* <br>

* #### get into root account <br>
sudo su - *get into the root account, using 'exit' to exit*<br>

* #### get groups and members <br>
cat /etc/group *get information about the groups*<br>
cat /etc/passwd *get more info about the groups*<br>

* #### change password <br>
passwd lilian *change password for user lilian*<br>
sudo passwd -e victor *force user victor to change passwd everytime re-enter the computer, -e means 'expire'*<br>

* #### add and remove users <br>
sudo useradd andra *add*<br>
sudo userdel andra *remove*<br>

* #### check permissions (read write & execute) of files <br>
ls -l filename <br>*output instance: -rwxr-r- 1 lilian  staff, the first 'rwx' means the rights for the owner of the file, the next 'r' represents the permission for the group members 'staff', and the last 'r' represents the permission for the other users*<br>

* #### modify permissions (read write & execute) of files <br>
chmod u+x filename  *u = user, g = group, o=everyone; + : add, - : remove; x = execute, r = read, w = write*<br>






* #### check if xxx software is installed<br>
dpkg -s xxx
* ####  update xxx software<br>
dpkg -s xxx sudo apt-get install -f<br>

* #### download software that is commonly used<br>
sudo apt-get update # make sure linux updated to the newest directory
sudo apt-get install firefox (etc.)
* #### delete software<br>
sudo apt-get remove xxx




<!--stackedit_data:
eyJoaXN0b3J5IjpbLTcxNjkwMTE4MiwtMTU2NzI3ODI5Nyw2NT
A0Mzg3NjgsMzUwMTU2NDk2LC02ODIyMzQxNTMsMTI3MTQ3ODMy
MCwtMjAzMDE0OTE3NSwtMTIzNjkyMDExLDE1Mzg4OTY2MDUsMj
cwMTMyMzM5LC0xNzgyMDQzOTQ2LC03MzEzOTA3NzUsNjI0OTQz
MzQ3LDE2MDA2MjE0NTMsLTEyNzcwODY0MTQsLTE3MTUxNzEyND
UsLTIwODY4MjM1MDcsODg2NTUzNjAzLC0xMzU0Mzg5MzAzLC01
ODM4NjgwNTZdfQ==
-->