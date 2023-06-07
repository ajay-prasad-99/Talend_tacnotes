
**Sudo Su**  => used to switch the user
            sudo => allows user to execute proper permissions
            su => switch user

**PWD**  (print current working directory):
 >useful to check the current location/directory of the file.
 
**CD**  ( Change directory):
    CD ..  => get the parent directory of the current directory
    CD -  => takes to the previous directory

**LS** (list): => list the files of the current directory

 1. Ls -a  => display all files, including hidden files from directory
 2. Ls -la  => display all files, including hidden files as in long format
 3. Ls -t  => Sort the files and dir list, by modified time
 4. Ls -r => Recursively list all the directories and sub-directories.

**SH** (shell), BASH (CMDline interpreter - can for administration and automation)

====>
1. **LS -ltr * sh**
 > Ls => List the files
 >-L => Show files in the Long format
 >-t  => Show(sort) the files/dir by the TIME modified
 >-r  => Reverse the sort order, show the newest files in last
 >*  => * is an Wildcard , It'll fetch the matching file with the ending as (.sh)
 >.sh => script file extension

2.  **PS -ef | grep -i TAC**
 
  >PS=> show the current process information, Fetch PID's (process ID)
         PID means => unique number asigned to each process in the server
    -ef   -e => Shows all the process
            -f => full listing, including CMD line Arguments 
     |  => Pipe operator , used to combine the commands
     grep => search pattern with specified name
     -i => option makes case-insensitive (tac or TAC)
*This will return all running Processes.*

3. **Ls -ltr**
 > ls => list
 > -l => Long format                      
 > -t => time modified
 > -r => reverse the sort , recent at last 
 > *specified directory in Long format*

4. **LS -ltr | wc -|**
  > Wc (word count) =>  display the number of lines, words, or char in the files
  > -|   => combine the count
  >
  *wc -l  => counts the line
  wc -w => counts the words
  wc -c => counts the char

5. **./ STOP**
> Stop => stop the process
> ./   => in current directory itself

6. **./ START**
    Start => start the process
    ./ => in current directory itself

7. **rm -rf** (Dangerous command - recovering hard)
> rm => "remove"
> -rf 
>   -r=> remove recursively
>   -f => "force", forcefully remove 
>             (Delete without prompting the confirmation)

8. **Crontab -l**
   > used to list current cronjobs for a specific user
   > cronjobs=> are specific jobs, schedule to run automatically on specific times
   These jobs on file called as Crontab.
 i,e. crontab -I , displays the current job the user.

9. **Df -h**
>-h => "*human reaable*" (gives size on readable format MB, GB)
>df => "disk free" (gives available space)
>
==> df -h, gives (Usage, Capacity, System type, total space, used space, available space, And percentage of those space's)

10. **Free -g**
> used to display amount of free and used memory, alsp swap space.
> -g => output as on gigabytes.
> 
> NOTE: "free", command only get memory usage , not disk space usage

11. **TOP (Useful to monitor, process, system performance, troubleshoot issues)**
 > It provides a detail view of the process running on the system
 > (memory, CPU usage, Priority, and other info's)
 > 
 > *highest CPU USAGE list on top*
 > 
 > TOP => Informations ::::::
 > (TIME, Uptime, Tasks (running /stopped), Total CPU cores, Load avg past 1, 10,15 min, Total Physical memory, Swap space , percentage of space)
 >
 > TOP => Process ::::::::
 > (PID, Owner, Priority, CPU percentage, memory, virtual memory size, status, CMD started process info)
 
 12. **WHOAMI**
 > view current username
 
 13. **Touch 'filename'**
 > creates new file or change timestamp on existing file
 > EX: touch adminsession.txt
 > can't changr the content of the file
 
 14. **Vi 'filename'**
 > Used to open or edit a file in the vi/vim editor
 > :::::::::::::
 > // *Vi is a powerful, terminal-based text editor that is known for its efficiency and flexibility. It is a modal editor, meaning that it has different modes for input and navigation. The two main modes are the command mode and the insert mode.* 

15. **Cat 'filename'**
> used to view the contents of the given file

 16.  **Mkdir 'directoryname'**
 > used to create the new directory
 > *For example, `mkdir -p data/images` will create a directory "data" if it doesn't exist*
 
 17. **Chmod '777'**
 > Used to change the perms of the file or dir
 > ////
 > *where "777" is an example of an octal mode. In this notation, each digit represents the permissions for the file's owner, its group, and others, respectively. Each digit is composed of three binary digits, representing read, write, and execute permissions, respectively. A 7 would be 111 in binary, which means that the owner has read, write, and execute permissions.*
 > ////
 > "chmod 777 filename" would give read, write, and execute permissions to the owner, group, and others for the file named "filename".
 
 18. **CP 'filename' path**
 >Used to copy files and directories
 >EX: cp myfile.txt /data
 >/////
 >*Can also use the "-r" option to copy directories and their contents recursively. For example, `cp -r mydir newdir` will copy the directory "mydir" and all its contents to a new directory named "newdir".

19. **:wq**
> Save and exit in Vi editor

20. **:q**
> Quit, without save the changes in the Vi editor


