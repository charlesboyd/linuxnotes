#Linux Notes
My personal list of notes and shell (bash) commands I've found usefull.
All paths below can be either relative or absolute, regardless of the type shown.  
By [Charles Boyd](http://charlesboyd.me/?ref=github-linuxnotes)  

---

##Basic Shell Commands
**Display the path of the current working directory**  
`pwd`  

**Change working directory**  
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

##Environment
**Show one environment variable** (This example: $HOME)  
`echo $HOME`  

**Show all  environment variables**  
`env`  

**PATH var save change** (Add the following line to the end of `~/.bashrc`)  
`export PATH=$PATH:/path/to/dir/`  


##Permissions and Ownership
**Change permissions of a file/directory**  
`chmod [perm] filename`  
Where [perm] can be several different [string types](http://www.grymoire.com/Unix/Permissions.html#uh-2)  

**Change the owner of a file/directory**  
`chown newowner file.txt`
* -R = Operate on files and directories recursively.

##DNS
**IP DNS Lookup**  
`dig google.com`  

**Revere-IP DNS lookup**  
`dig -x 8.8.8.8`  


##File Display and Console Output
**Display an entire file**  
`cat filename`  
*OR*  
`cat < filename`  

**Add line numbers to `cat` output**  
`cat filename | nl`

**Octal dump**  
`od -cb filename.txt`

**Output to file and to the screen**  
`command -option | tee log.txt`  

##GUI and Detaching
**Open chrome to a URL**  
`google-chrome bing.com`  

**Open GUI Application and detact from terminal**  
`gedit &!`  
*OR*  
`nohup google-chrome "http://charlesboyd.me" </dev/null &>/dev/null &!`  


##Third-Party
**Weather**  
`curl wttr.in/city_name`  
  
  
##Shell Scripting  
**Save output to a bash variable** (Example command: `ls -l`)  
`MYVAR="$(ls -1)"`  

**Print saved bash variable**   
`echo "${MYVAR}"`  
  
##Files and directories  
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

**Create link (or "shortcut")**  
`ln -s /path/to/target /the/link/name`
* -s = [soft link](http://askubuntu.com/questions/108771/what-is-the-difference-between-a-hard-link-and-a-symbolic-link)

##Logins  
**Log into mySQL**  
`mysql -u root -p`  

**SSH to host** (And forward ports; e.g. Local port 13306 to remote's local port 3306)  
`ssh username@example.com -L 13306:localhost:3306`

**Shutdown**  
`sudo shutdown -h now`  
*or*  
`sudo poweroff`  


##Client/Server  
**Output HTTP Responce**
`curl example.com`  
* -d "Payload here" = Send this data in request and change type to POST  
* -X PUT = Change type of request (example: change to PUT)    

**Retrieve and save remote file to working directory**
`wget example.com/filename`


##Searches  
*TODO*  


##Common Tools  
**Text editors**  
`nano`  
*or*  
`vi`  

**Package Manager** (e.g. install)  
`apt-get install packagename`  


##Simple Commands  
 **Display Current Date/Time**  
`date`  

**Display Running Processes**  
`top`  

**Clear the console display**  
`clear` 

**Output a given string**  
`echo "Hello World"`  

**Print the current user's name**  
`whoami` 

**Display network configuration**  
`ifconfig`  
*or*
`ifconfig /all`  

**Display Mail Queue**  
`mailq`  
