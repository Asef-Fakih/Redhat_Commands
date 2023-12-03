# Linux Command Cheat Sheet
## File Commands
  > ls - The most frequently used command in Linux to list directories
> ls -a shows hidden files in addition to the visible ones.
> pwd - Print working directory command in Linux
> cd - Linux command to navigate through directories
> mkdir - Command used to create directories in Linux
> mkdir -p  mkdir -p Music/2020/Songs will make the new “2020” directory.
> mkdir sa{1..50} will create directories from sa 1 to 50
> rm  lets you delete a file or directory passing its name
> rm -d lets you delete a directory passing its name
> cp file1 file2 copy file1 to file2
> cp file1 dir1 copy the file into the directoty
> mv file1 dir1 move file file1 ro dir1
> touch creates file
> cat reads file contents
> more file - ourputs the contents of the file
> head file1 outputs the first 10 lines of file1
> tail file1 outputs the Last 10 lines of file1
> ~ go to root
> cd .. go back one step
> 

## Process related commands
> ps: Display information about running processes.
> top: Display and update sorted information about system processes in real-time.
> kill PID Terminate or signal a process.
> killall process_name Kill processes by name.
> jobs: Display status of jobs in the current session.
> fg – brings the most recent job to foreground

## file permission
> chmod u+rwx,go=rx file.txt This command adds read, write, and execute permissions for the owner (u) and removes all permissions for the group (g) and others (o) on the file.txt.
> umask 077 determines the default permissions assigned to newly created files and directorie, so a umask of 022 will result in permissions of 755 for directories and 644 for files (since 777 - 022 = 755 and 666 - 022 = 644)
> Passwd set password for user
> passwd -d delete password for user
> passwd -u -l Unlock and lock passwords
> gpasswd group_name set password for group
> gpasswd -a pavan,john developer add multiple users to group
> gpasswd -A joy group_name set user joy a manager to group
> chown new_owner filename change the owner of a file
> chown new_owner:new_group filename Change the owner and group of a file:
> adduser add new user
> adduser -m user creates home directory
> adduser -g add users primary group
> adduser -G add users secondary group
> adduser -s bin/bash user add bin bash shell to the user
> adduser -h /home/user_custom user Specify the home directory for user
> groupadd add new group
> groupadd -g 1001 mygroup Set the group id for the group
> Chmod + s "-rwsr-xr-x. 1 root root 33544 Dec 13  2019 /usr/bin/passwd" ad, file with **SUID** always executes as the user who owns the file
> chmod g+s directoryname  For directories, when the SGID permission is set, new files created within that directory inherit the group ownership of the parent directory
> chmod +t directoryname When the sticky bit is set on a directory, only the owner of a file within that directory can delete or rename the file, regardless of the write permissions of other users on the same directory.
> userdel -r 'username' delete user
> usermod -a -G GROUPNAME USERNAME add user to a group
> usermod -u new_uid username change user id
> usermod -l new_user old_user change username
> usermod -s change login shell
> usermod -l username display user info
> deluser USER GROUPNAME remove user from user group
> ll -d dir too see details permissions for directory
> ll -a shows hidden files
> ll -h shows human readable version
> Stat shows details and access of the directory
> id  user to see details of that user 
