#Linux Notes
My personal list of notes and shell commands I've found usefull  
By [Charles Boyd](http://charlesboyd.me/?ref=github-linuxnotes)  

---

##Single Shell Commands
**Display Mail Queue**  
`mailq`  
    
---
    
##United Shell Commands 
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


###Console Outout  
**Output to file and to the screen**  
`command -option | tee log.txt`


###Other
**Open chrome to a URL**  
`google-chrome bing.com`  

**Open GUI Application and detact from terminal**  
`gedit &!`  
-OR-  
`nohup google-chrome $urltoopen </dev/null &>/dev/null &!`  

**Save output to a bash variable** (Example command: `ls -l`)  
`OUTPUT="$(ls -1)"`  
`echo "${OUTPUT}"`  

