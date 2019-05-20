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
mv ~/yellow.txt ~/blue.txt *rename file without*<br>
mv ~/yellow.txt ~/lilian<br>

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
eyJoaXN0b3J5IjpbLTg1Njk5NTE2NSwtMjA4NjgyMzUwNyw4OD
Y1NTM2MDMsLTEzNTQzODkzMDMsLTU4Mzg2ODA1NiwxMDU1ODg2
ODMsLTg5Nzc5ODU1NSwtMTI2OTc3ODYwMV19
-->