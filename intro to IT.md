## Basic Code for Bash/Zsh

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

* #### check if xxx software is installed<br>
dpkg -s xxx
* ####  update xxx software<br>
dpkg -s xxx sudo apt-get install -f<br>
* #### remove files and directories<br>
rm ~/yellow.txt *remove a file*<br>
rm -r ~/my_file *remove a directory*<br>
* #### display file contents<br>
cat ~/yellow.txt <br> *display the whole file*
less ~/large_file.txt<br> *display the first page, and use enter to go by lines, use tab to go by pages, and q to quit*


* #### download software that is commonly used<br>
sudo apt-get update # make sure linux updated to the newest directory
sudo apt-get install firefox (etc.)
* #### delete software<br>
sudo apt-get remove xxx




<!--stackedit_data:
eyJoaXN0b3J5IjpbODE1NTYyMDc5LC0xMjc3MDg2NDE0LC0xNz
E1MTcxMjQ1LC0yMDg2ODIzNTA3LDg4NjU1MzYwMywtMTM1NDM4
OTMwMywtNTgzODY4MDU2LDEwNTU4ODY4MywtODk3Nzk4NTU1LC
0xMjY5Nzc4NjAxXX0=
-->