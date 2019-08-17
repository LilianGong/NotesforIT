>## Basic Command Lines for LINUX

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
ls -ld directory *show the permission for a directory*<br>

* #### modify permissions (read write & execute) of files <br>
sudo chmod u+x filename  *u = user, g = group, o=everyone; + : add, - : remove; x = execute, r = read, w = write*<br>
sudo chmod ugo-x filename  *u = user, g = group, o=everyone; + : add, - : remove; x = execute, r = read, w = write*<br>
sudo chmod a+rwx filename *add permissions to all, a stands for all* <br>
sudo chmod 754 filename  <br>
*1 = execute, 2 = write, 4 = read; each number represents seperately by the sequence of user, group and other person*<br>
sudo chown joe filename *change the owner of the file to joe *<br>
sudo chgrp best-group filename *change the group of the file to best-group* <br>

* #### installation of softwares<br>
dpkg -s xxx*'s' flag refers to search if xxx.deb is installed*<br>
dpkg -i xxx.deb *'i' flag refers to install xxx.deb* <br>
dpkg -r xxx.deb *'r' flag refers to uninstall xxx.deb* <br>
dpkg -l  *'l' flag refers to list all installed packages* <br>

##### for mac OS:<br>

install homebrew <br>
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"<br>
brew install <br>
brew uninstall <br>
brew list<br>
brew -v  *check version*<br>
brew cask install *install software with GUI* <br>

* #### Archive in LINUX<br>
tar -cvf tarname.tar file1  file2 file3 *make tarfile with file1*<br>
tar -xvf tarname.tar *extract tarname.tar*<br>


* ####  update xxx software<br>
dpkg -s xxx sudo apt-get install -f<br>


* #### download software that is commonly used<br>
sudo apt-get update # make sure linux updated to the newest directory
sudo apt-get install firefox (etc.) <br>
sudo apt install -f *fix the missing dependencies*<br>
* #### delete software<br>
sudo apt-get remove xxx<br>


* ####  OS system update<br>
uname -r *check for the OS kernel version* <br> 
apt  full-upgrade *upgrade the OS system, but do remember to 'apt update' first to update the application sources* <br> 

* ####  Partition Management<br>
lsblk *list all partitions*<br>
parted -l *show all the partitions that connected to the computer* <br>

sudo parted /dev/sdb --> print *enter the parted command line and show the infomation of the disk* <br>

Mklabel gpt *mark the disk with gpt table* <br>

mkpart primary ext4 1MiB 5 GiB *make a partition named as primary with ext4 file system, starting at 1 MiB and ending at 5 GiB* <br>

quit --> mkfs  -t ext4 /dev/sdb1 *format the partition with the file system using mkfs*<br>

sudo mount /dev/sdb1 /my-usb *mount the partition*<br>
du -h *show disks usage* <br> 

* ####  about Shells<br>
cat /etc/shells *check for the OS kernel version* <br> 
echo $SHELL *check the current shell that is being used* <br> 
chsh -s  *check the current shell that is being used* <br> 






<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk0NDIzOTYzMiwxNTY4NTE2NDMsLTE0Nj
ExODU0NDVdfQ==
-->