#Linux Notes
My personal list of notes and shell (bash) commands I've found usefull  
By [Charles Boyd](http://charlesboyd.me/?ref=github-linuxnotes)  


---
    
    
##Useful Shell Commands 
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
-OR-  
`cat < filename`  

**Add line numbers to `cat` output ("nl")**  
`cat filename | nl~`

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
-OR-  
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
  * -f = follow   
  * -F = follow and retry  
`tail -f filename.txt`  

**Watch directory changes**  
`watch "ls -lrt | tail -10"`  


###Logins
**Log into mySQL**  
`mysql -u root -p`  

**SSH to server** (And forward local port 13306 to remote local port 3306)  
`ssh username@example.com -L 13306:localhost:3306`


###Other
**Display Mail Queue**  
`mailq`  

