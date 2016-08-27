#Linux Notes
My personal list of notes and shell (bash) commands I've found usefull  
By [Charles Boyd](http://charlesboyd.me/?ref=github-linuxnotes)  


---
    
    
##Useful Shell Commands  
###Basics
**Display the path of the current working directory**  
`pwd`  

**Change working directory**  
`cd subfolder`  
*OR*  
`cd /path/to/directory`  

**Directory listing**  
`ls`  
*OR*  
`ls -la /path/to/directory`  
* -l = List  
* -a = All Files  

**Make directory**  
`mkdir directoryname`  

**Remove file or directory**  
`rm /path/to/thing`  
*OR*  
`rm -r directory`  
* -r = Recursive (required if directory has things in it) 

**Change user** (E.g. change to `otherperson`)  
`su otherperson`  

**Run as super user**  
`sudo command --option`  

**Change password**  
`passwd`  

**Get infomation on a command** (Example: `ls`)  
`man ls`

**Show shell history**  
`history`  

**Exit the shell**  
`exit` 

###Environment
**Show one environment variable** (This example: $HOME)  
`echo $HOME`  

**Show all  environment variables**  
`env`  

**PATH var save change** (Add the following line to the end of `~/.bashrc`)  
`export PATH=$PATH:/path/to/dir/`  


###DNS
**IP DNS Lookup**  
`dig google.com`  

**Revere-IP DNS lookup**  
`dig -x 8.8.8.8`  


###File Display  
**Display an entire file**  
`cat filename`  
*OR*  
`cat < filename`  

**Add line numbers to `cat` output**  
`cat filename | nl`

**Octal dump**  
`od -cb filename.txt`

###Console Outout  
**Output to file and to the screen**  
`command -option | tee log.txt`

###GUI and Detaching
**Open chrome to a URL**  
`google-chrome bing.com`  

**Open GUI Application and detact from terminal**  
`gedit &!`  
*OR*  
`nohup google-chrome "http://charlesboyd.me" </dev/null &>/dev/null &!`  

###Third-Party
**Weather**  
`curl wttr.in/city_name`  
  
###Shell Scripting
**Save output to a bash variable** (Example command: `ls -l`)  
`OUTPUT="$(ls -1)"`  
`echo "${OUTPUT}"`  
  
###Files and directories
**Updates access time of file OR create if it does not exist**  
`touch filename.txt`

**Directory sizes (human readable)**  
`du -h`

**Watch file updates**  
`tail -f filename.txt`  
* -f = follow  
* -F = follow and retry  

**Watch directory changes**  
`watch "ls -lrt | tail -10"`  


###Logins
**Log into mySQL**  
`mysql -u root -p`  

**SSH to host** (And forward ports; e.g. Local port 13306 to remote's local port 3306)  
`ssh username@example.com -L 13306:localhost:3306`


###Client/Server
**Output HTTP Responce**
`curl example.com`  
* -d "Payload here" = Send this data in request and change type to POST  
* -X PUT = Change type of request (example: change to PUT)    

**Retrieve and save remote file to working directory**
`wget example.com/filename`

###Common Tools
**Text editors**  
`nano`  
*or*  
`vi`  

###Simple Commands  
 **Display Current Date/Time**  
`date`  

**Display Running Processes**  
`top`  

**Output a given string**  
`echo "Hello World"`  

**Display Mail Queue**  
`mailq`  
