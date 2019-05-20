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

* #### remove files and directories<br>
rm ~/yellow.txt *remove a file*<br>
rm -r ~/my_file *remove a directory*<br>

* #### display file contents<br>
cat ~/yellow.txt  *display the whole file*<br> 
less ~/large_file.txt *display the first page, and use enter /down to go by lines, use tab to go by pages, q to quit, g to the first line, G to the end of the file, and /word_search to search for certain words/phrases* <br> 
head large_file.txt *head 10 lines in the file* <br>
tail large_file.txt *tail 10 lines in the file* <br>


* #### search within files<br>
grep import *.py *search 'import' in all python files* <br>

*#### I/O redirect <br>
echo woof > dogs.txt *put a word in  a file that overwrite the previous contents*<br>
echo woof >> dogs.txt *put a word in  a file without overwriting the previous contents*<br>
ls ~/non_exist.txt 2> /dev/null *output the standard error* <br>

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
eyJoaXN0b3J5IjpbLTE3ODIwNDM5NDYsLTczMTM5MDc3NSw2Mj
Q5NDMzNDcsMTYwMDYyMTQ1MywtMTI3NzA4NjQxNCwtMTcxNTE3
MTI0NSwtMjA4NjgyMzUwNyw4ODY1NTM2MDMsLTEzNTQzODkzMD
MsLTU4Mzg2ODA1NiwxMDU1ODg2ODMsLTg5Nzc5ODU1NSwtMTI2
OTc3ODYwMV19
-->