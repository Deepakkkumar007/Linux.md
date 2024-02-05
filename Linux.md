# Linux Assignment 4
## 1.Create a directory named "MyFiles" in your home directory. Navigate into this directory and list its contents.
Ans-  
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ mkdir myfiles
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ ls
 anydesk          Desktop        file1       file_list.txt                            latest            machine         MyFiles               snap               ubuntu-20.04.3-desktop-amd64.iso
 backup           directory      file1.txt   fileZ                                    link1             Music           my_notes.txt         'sudo apt update'   Videos
 Bash             Documents      file2       get-docker.sh                            link2             my_dir          Pictures              symlink            virtual
 conf_files.txt   document.txt   file2.txt   google-chrome-stable_current_amd64.deb   link_dir          my_directory2   Public                symlink2
 deepak2          Downloads      file54      index.html                               links_directory   myfiles        'Redhat id password'   Templates
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cd myfiles/
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ touch s f h j
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ls
f  h  j  s
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ 
```



# 2.Copy a file named "document.txt" from your home directory to the "MyFiles" directory. Move the file to a subdirectory named "Documents" within "MyFiles."
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ mkdir Documentss
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ls
Documentss  f  h  j  s
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ cd
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ touch document1.txt 
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ ls
 anydesk          Desktop         Downloads   file54                                   index.html   links_directory   myfiles       'Redhat id password'   Templates
 backup           directory       file1       file_list.txt                            latest       machine           MyFiles        snap                  ubuntu-20.04.3-desktop-amd64.iso
 Bash             document1.txt   file1.txt   fileZ                                    link1        Music             my_notes.txt  'sudo apt update'      Videos
 conf_files.txt   Documents       file2       get-docker.sh                            link2        my_dir            Pictures       symlink               virtual
 deepak2          document.txt    file2.txt   google-chrome-stable_current_amd64.deb   link_dir     my_directory2     Public         symlink2
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cp document.txt myfiles
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cd myfiles/
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ls
Documentss  document.txt  f  h  j  s
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cd myfiles/
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ mv document.txt Documentss
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ls
Documentss  f  h  j  s
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ cd Documentss
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss$ ls
document.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss$ 
```



# 3.Create an empty file named "notes.txt" in the "MyFiles" directory. Afterward, delete the file.
Ans-  
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ls
Documentss  f  h  j  s
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ > notes.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ls
Documentss  f  h  j  notes.txt  s
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ rm notes.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ls
Documentss  f  h  j  s
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ 
```


# 4.Create a hard link named "hardlink.txt" for the file "document.txt" within the "Documents" subdirectory. Also, create a symbolic link named "symlink.txt" in the same location.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ls
Documentss  f  h  j  s
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ cd Documentss
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss$ ls
document.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss$ cd
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cd myfiles
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ls
Documentss  f  h  j  s
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ > notes.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ls
Documentss  f  h  j  notes.txt  s
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ rm notes.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ls
Documentss  f  h  j  s
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ cd Documentss
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss$ ls
document.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss$ ln document.txt hardlink1.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss$ ls -lrth
total 0
-rw-rw-r-- 2 deepak deepak 0 Feb  3 22:25 hardlink1.txt
-rw-rw-r-- 2 deepak deepak 0 Feb  3 22:25 document.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss$ ln -s document.txt symlink.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss$ ll
total 8
drwxrwxr-x 2 deepak deepak 4096 Feb  5 10:35 ./
drwxrwxr-x 3 deepak deepak 4096 Feb  3 22:39 ../
-rw-rw-r-- 2 deepak deepak    0 Feb  3 22:25 document.txt
-rw-rw-r-- 2 deepak deepak    0 Feb  3 22:25 hardlink1.txt
lrwxrwxrwx 1 deepak deepak   12 Feb  5 10:35 symlink.txt -> document.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss$ 
```



# 5.In the "MyFiles" directory, use a single command to list all files that start with the letter "a" and have a ".txt" extension.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cd myfiles
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ touch aa.txt aab.txt bcd.txt abc.txt dd.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ls
aab.txt  aa.txt  abc.txt  bcd.txt  dd.txt  Documentss  f  h  j  s
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ cd
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ find ~/myfiles -type f -name 'a*.txt'
/home/deepak/myfiles/abc.txt
/home/deepak/myfiles/aa.txt
/home/deepak/myfiles/aab.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
```

# 6.Rename all files in the "Documents" subdirectory of "MyFiles" with a ".bak" extension. Ensure the original file names are preserved.
Ans- 
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cd myfiles
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ls
aab.txt  aa.txt  abc.txt  bcd.txt  dd.txt  Documentss  f  h  j  s
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ cd Documents
bash: cd: Documents: No such file or directory
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ for file in *; do
> mv "$file" "${file}.bak"
> done
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ll
total 12
drwxrwxr-x  3 deepak deepak 4096 Feb  5 10:44 ./
drwxr-xr-x 36 deepak deepak 4096 Feb  3 22:25 ../
-rw-rw-r--  1 deepak deepak    0 Feb  5 10:39 aab.txt.bak
-rw-rw-r--  1 deepak deepak    0 Feb  5 10:39 aa.txt.bak
-rw-rw-r--  1 deepak deepak    0 Feb  5 10:39 abc.txt.bak
-rw-rw-r--  1 deepak deepak    0 Feb  5 10:39 bcd.txt.bak
-rw-rw-r--  1 deepak deepak    0 Feb  5 10:39 dd.txt.bak
drwxrwxr-x  2 deepak deepak 4096 Feb  5 10:35 Documentss.bak/
-rw-rw-r--  1 deepak deepak    0 Feb  3 22:22 f.bak
-rw-rw-r--  1 deepak deepak    0 Feb  3 22:22 h.bak
-rw-rw-r--  1 deepak deepak    0 Feb  3 22:22 j.bak
-rw-rw-r--  1 deepak deepak    0 Feb  3 22:22 s.bak
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ 
```

# Use a wildcard character to copy all files from the "Documents" subdirectory of "MyFiles" to another directory named "Backup."
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cd myfiles
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ ls
aab.txt.bak  aa.txt.bak  abc.txt.bak  bcd.txt.bak  dd.txt.bak  Documentss.bak  f.bak  h.bak  j.bak  s.bak
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ cd Documentss.bak
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss.bak$ ls
backup  document.txt  hardlink1.txt  symlink.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss.bak$ cd
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cp -r ~/myfiles/Documentss.bak/* ~/myfiles/backup/
cp: target '/home/deepak/myfiles/backup/' is not a directory
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cp -r ~/myfiles/Documentss.bak/* ~/myfiles/Backup/
cp: target '/home/deepak/myfiles/Backup/' is not a directory
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cp -r ~/myfiles/Documentss.bak/* ~/myfiles/backup/
cp: target '/home/deepak/myfiles/backup/' is not a directory
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cd myfiles
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ cd Documentss.bak
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss.bak$ mkdir Backupp
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss.bak$ ls
backup  Backupp  document.txt  hardlink1.txt  symlink.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Documentss.bak$ cd
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$  cp -r ~/myfiles/Documentss.bak/* ~/myfiles/Backupp/
cp: target '/home/deepak/myfiles/Backupp/' is not a directory
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ mkdir ~/myfiles/Backupp
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cp -r ~/myfiles/Documentss.bak/* ~/myfiles/Backupp/
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ ls
 anydesk          Desktop         Downloads   file54                                   index.html   links_directory   myfiles       'Redhat id password'   Templates
 backup           directory       file1       file_list.txt                            latest       machine           MyFiles        snap                  ubuntu-20.04.3-desktop-amd64.iso
 Bash             document1.txt   file1.txt   fileZ                                    link1        Music             my_notes.txt  'sudo apt update'      Videos
 conf_files.txt   Documents       file2       get-docker.sh                            link2        my_dir            Pictures       symlink               virtual
 deepak2          document.txt    file2.txt   google-chrome-stable_current_amd64.deb   link_dir     my_directory2     Public         symlink2
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cd myfiles
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles$ cd  Backupp
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Backupp$ ls
backup  Backupp  document.txt  hardlink1.txt  symlink.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~/myfiles/Backupp$ 
```



# 8.Execute the ls command to list files in the current directory. Save the output to a file named "file_list.txt." Then, use a pipe to filter the output through grep to display only files with a ".txt" extension.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ ls >file_list.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ ls
 anydesk          Desktop         Downloads   file54                                   index.html   links_directory   myfiles       'Redhat id password'   Templates
 backup           directory       file1       file_list.txt                            latest       machine           MyFiles        snap                  ubuntu-20.04.3-desktop-amd64.iso
 Bash             document1.txt   file1.txt   fileZ                                    link1        Music             my_notes.txt  'sudo apt update'      Videos
 conf_files.txt   Documents       file2       get-docker.sh                            link2        my_dir            Pictures       symlink               virtual
 deepak2          document.txt    file2.txt   google-chrome-stable_current_amd64.deb   link_dir     my_directory2     Public         symlink2
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ grep '\.txt$' file_list.txt
conf_files.txt
document1.txt
document.txt
file1.txt
file2.txt
file_list.txt
my_notes.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
```



# 9.Create a new text file named "my_notes.txt" using the touch command. Open the file in the Vim editor, add some text, and save the changes.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ touch my_notes.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ vim my_notes.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
```


# 10.Run the date command and store the output in a variable named "current_date." Display the value of the variable and append it to the "my_notes.txt" file.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ current_date=$(date)
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ echo "Current Date: $current_date"
Current Date: Monday 05 February 2024 11:07:54 AM IST
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ echo "Current Date: $current_date" >> my_notes.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cat my_notes.txt
i love linux
Current Date: Friday 02 February 2024 05:10:18 PM IST
This is a new line of text.
i am a linux love
r
:%s/important/critical/g

Current Date: Monday 05 February 2024 11:07:54 AM IST
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
```


# 11.Edit the Bash startup script (e.g., .bashrc) to set an environment variable named "CUSTOM_PATH" to a specific directory path. Ensure the variable is available in new shell sessions.
Ans-




# 12.Use the echo command to add a new line of text to the "my_notes.txt" file without overwriting existing content. Verify that the new text is appended.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ echo "linux lover" >>my_notes.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cat my_notes.txt
i love linux
Current Date: Friday 02 February 2024 05:10:18 PM IST
This is a new line of text.
i am a linux love
r
:%s/important/critical/g

Current Date: Monday 05 February 2024 11:07:54 AM IST
linux lover
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
```



# 13.List all files in the "/etc" directory, filter the output to include only those containing the word "conf," and save the result to a file named "conf_files.txt."
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ find /etc -type f -name "*conf*" > conf_files.txt
find: ‘/etc/polkit-1/localauthority’: Permission denied
find: ‘/etc/libvirt/secrets’: Permission denied
find: ‘/etc/chatscripts’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/etc/ppp/peers’: Permission denied
find: ‘/etc/cups/ssl’: Permission denied
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo find /etc -type f -name "*conf*" > conf_files.txt
[sudo] password for deepak: 
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ cat conf_files.txt
/etc/hdparm.conf
/etc/dhcp/dhclient.conf
/etc/rsyslog.conf
/etc/e2scrub.conf
/etc/nginx/snippets/snakeoil.conf
/etc/nginx/snippets/fastcgi-php.conf
/etc/nginx/nginx.conf
/etc/nginx/fastcgi.conf
/etc/default/im-config
/etc/geoclue/geoclue.conf
/etc/sane.d/sceptre.conf
/etc/sane.d/net.conf
/etc/sane.d/qcam.conf
/etc/sane.d/snapscan.conf
/etc/sane.d/u12.conf
/etc/sane.d/microtek.conf
/etc/sane.d/canon.conf
/etc/sane.d/coolscan3.conf
/etc/sane.d/tamarack.conf
/etc/sane.d/dc25.conf
/etc/sane.d/avision.conf
/etc/sane.d/apple.conf
/etc/sane.d/leo.conf
/etc/sane.d/gphoto2.conf
/etc/sane.d/umax.conf
/etc/sane.d/rts8891.conf
/etc/sane.d/dmc.conf
/etc/sane.d/umax1220u.conf
```




# 14.Open the "my_notes.txt" file in Vim. Use Vim's search and replace functionality to replace all occurrences of the word "important" with "critical." Save the changes.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ vim my_notes.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
In vim editor, after pressing esc type
:%s/important/critical/g
```


# 15.Create a new user account named "john_doe." Set the user's home directory to "/home/john_doe" and assign the user to the "users" group.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo adduser --home /home/john_doee --ingroup users john_doee
Adding user `john_doee' ...
Adding new user `john_doee' (1008) with group `users' ...
Creating home directory `/home/john_doee' ...
Copying files from `/etc/skel' ...
New password: 
Retype new password: 
passwd: password updated successfully
Changing the user information for john_doee
Enter the new value, or press ENTER for the default
	Full Name []: 
	Room Number []: 
	Work Phone []: 
	Home Phone []: 
	Other []: 
Is the information correct? [Y/n] y
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ id john_doee
uid=1008(john_doee) gid=100(users) groups=100(users)
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
```



# 16.Add the user "john_doe" to the sudoers file, allowing them superuser privileges. Confirm that "john_doe" can execute commands with sudo.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo visudo
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo ls /root
snap  test.txt
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
```


# 17.Modify the user account "john_doe" to change the default shell to "/bin/bash" and set the account's expiration date to one month from today.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo chsh -s /bin/bash john_doee
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo adduser john_doee development_team
adduser: The group `development_team' does not exist.
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo chage -E $(date -d "+1 month" +"%Y-%m-%d") john_doe
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo chage -E $(date -d "2022-03-15 month" +"%Y-%m-%d") john_doee
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ getent passwd john_doee
john_doee:x:1008:100:,,,:/home/john_doee:/bin/bash
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo chage -l john_doee
Last password change					: Feb 05, 2024
Password expires					: never
Password inactive					: never
Account expires						: Apr 15, 2022
Minimum number of days between password change		: 0
Maximum number of days between password change		: 99999
Number of days of warning before password expires	: 7
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
```



# 18.Create a new group named "development_team." Add "john_doe" to this group and verify the group's existence.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo groupadd development_team
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo usermod -aG development_team john_doee
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ grep development_team /etc/group
development_team:x:1010:john_doee
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ getent group development_team
development_team:x:1010:john_doee
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
```


# 19.Remove "john_doe" from the "users" group and add them to the "development_team" group. Confirm the changes.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo deluser john_doee users
/usr/sbin/deluser: You may not remove the user from their primary group.
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo usermod -aG development_team john_doee
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ id john_doee
uid=1008(john_doee) gid=100(users) groups=100(users),1010(development_team)
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo deluser john_doee users
/usr/sbin/deluser: You may not remove the user from their primary group.
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo usermod -aG development_team john_doee
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ id john_doee
uid=1008(john_doee) gid=100(users) groups=100(users),1010(development_team)
```


# 20.Delete the user account "john_doe" and ensure that their home directory is also removed.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo userdel -r john_doee
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
```

# 21.Delete the group "development_team" and ensure that all users previously belonging to the group are appropriately handled.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo groupdel development_team
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
```


# 22.Implement a password policy that requires users to change their passwords every 90 days. Apply this policy to all existing and new user accounts.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo chage -M 98 -I -1 -E -1 sumit
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
```


# 23.Manually lock the user account "john_doe." Attempt to log in as "john_doe" to confirm that the account is locked. Then, unlock the account.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo passwd -l sumit
passwd: password expiry information changed.
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ su - sumit
Password: 
su: Authentication failure
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo passwd -u sumit
passwd: password expiry information changed.
```


# 24.Use the id command to display detailed information about the "john_doe" user, including user ID, group ID, and supplementary groups.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ id sumit
uid=1001(sumit) gid=1003(chaubey) groups=1003(chaubey)
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
```


# 25.Configure the password aging for the user "john_doe" to enforce a maximum password age of 60 days. Confirm that the changes take effect.
Ans-
```
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo chage -M 60 john_doee
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ sudo chage -l john_doee
Last password change					: Feb 05, 2024
Password expires					: Apr 05, 2024
Password inactive					: never
Account expires						: never
Minimum number of days between password change		: 0
Maximum number of days between password change		: 60
Number of days of warning before password expires	: 7
deepak@deepak-VivoBook-ASUSLaptop-X512FL-X512FL:~$ 
```





