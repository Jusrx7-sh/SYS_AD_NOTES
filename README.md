# Linux SYS_ADMIN Notes

#### This is My own Notes

#### This Repo Structed by days

---

## Day 1 : was Basics info & installation ;

## Day 2 & Day 3 :  Basics Commands ;

### Command Line Basics :

1. __`pwd`__
   
   ```bash
   $: pwd
   /home/xy
   ```

2. __`ls`__
   
   ```bash
   ls
   DBFiles  file1
   ```

3. **`su`**
   
   ```bash
   # Switch from user to nother user
   $: whoami # command tell you who are you .
   root 
   $: su - xy  # i will be xy user  
   ```

4. **`cal`**
   
   ```bash
   cal 2017
         January               February               March          
   
     Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa  
     1  2  3  4  5  6  7            1  2  3  4            1  2  3  4  
     8  9 10 11 12 13 14   5  6  7  8  9 10 11   5  6  7  8  9 10 11  
     15 16 17 18 19 20 21  12 13 14 15 16 17 18  12 13 14 15 16 17 18  
     22 23 24 25 26 27 28  19 20 21 22 23 24 25  19 20 21 22 23 24 25  
     29 30 31              26 27 28              26 27 28 29 30 31     
   
          April                  May                   June          
   
   Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa  
                      1      1  2  3  4  5  6               1  2  3  
    2  3  4  5  6  7  8   7  8  9 10 11 12 13   4  5  6  7  8  9 10  
    9 10 11 12 13 14 15  14 15 16 17 18 19 20  11 12 13 14 15 16 17  
   16 17 18 19 20 21 22  21 22 23 24 25 26 27  18 19 20 21 22 23 24  
   23 24 25 26 27 28 29  28 29 30 31           25 26 27 28 29 30     
   30                                                                
   
           July                 August              September        
   
   Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa  
                      1         1  2  3  4  5                  1  2  
    2  3  4  5  6  7  8   6  7  8  9 10 11 12   3  4  5  6  7  8  9  
    9 10 11 12 13 14 15  13 14 15 16 17 18 19  10 11 12 13 14 15 16  
   16 17 18 19 20 21 22  20 21 22 23 24 25 26  17 18 19 20 21 22 23  
   23 24 25 26 27 28 29  27 28 29 30 31        24 25 26 27 28 29 30  
   30 31                                                             
   
         October               November              December        
   
   Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa  
    1  2  3  4  5  6  7            1  2  3  4                  1  2  
    8  9 10 11 12 13 14   5  6  7  8  9 10 11   3  4  5  6  7  8  9  
   15 16 17 18 19 20 21  12 13 14 15 16 17 18  10 11 12 13 14 15 16  
   22 23 24 25 26 27 28  19 20 21 22 23 24 25  17 18 19 20 21 22 23  
   29 30 31              26 27 28 29 30        24 25 26 27 28 29 30  
                                               31 
   ```

5. **`date`**
   
   ```bash
   date
   Wed Jan 24 12:09:14 PM EET 2024
   ```

6. **`eject`** __disconnect with removable media__
   
   ```bash
   eject # eject only opens CD-ROM 
   eject /dev/sda # disconnect with sda drive 
   ```

<img title="" src="https://upload.wikimedia.org/wikipedia/commons/7/70/Sony_CRX310S-Internal-PC-DVD-Drive-Opened.jpg" alt="CD-ROM" width="787" data-align="center">

7. `TTY`'s and `chvt`
   
   ```bash
   tty # Get TTY number I in 
   chvt 5 # Change From TTY I in to TTY 5
   ```

### Linux File SYS Structure

<img src="https://1.bp.blogspot.com/-UQ7-sWd_J4w/WmhKIFx7_fI/AAAAAAAAHIE/tixi5SsyI5YzoJygq_JQKL50axe2cAcrQCLcBGAs/s1600/Untitled.png" title="" alt="CD-ROM" width="763">

* `home`    : home Direcetory of any user will be created

* `root`    :  root's Direcetory only for him 

* `boot`    :  boot files There

* `etc`      :  every Configration will be saved into it

* `bin`      : all bin files there 

* `sbin`    : system binarys For root only

* `dev`      :  devices file + Special Files ex __`/dev/null`__,__`/dev/zero`__ and more
  
  >           __`EVERY THING IS FILE in Linux`__

* `tmp`      : temp files 

* `usr`      : Shared File between users 

* `var`      : variable files for services Like Apache , FTP , SMTP , and so on  

* `media` , `mount` , `mnt`  : Mounting Points 
  
  ```bash
  mount /dev/sda1 /mnt/
  mount /dev/sdb1 /media/
  mount /dev/sdc1 /mount/
  or any another endpoint
  mount /dev/sda3 /usr/local_mount/
  ```

* `run` ,`sys` , `proc`   :  Kernel handle then + services info there and Hardware info There  

* `opt`,`srv`      : optinal files __you can remove it___

* `lib`      :  Library files like for __`iostream`__ for c++ and so on with another lang 

---

### some Short-Cuts

```bash
SHORT-CUTs
cd - # return you into last directory you was there
cd ~username == cd /home/username 
touch file1 # Creating New file called file1 
touch file{1..4} # Create 4 Files starts from 1 to 4 called fileX
mkdir dir{1..50..2}#  for i=1 ; i>50 ; i+2
Demo :
$: touch file{15..300..15}
$: ls 
file105  file135  file150  file180  file210  file240  file270  file30   file45  file75
file120  file15   file165  file195  file225  file255  file285  file300  file60  file90
```

---

## Day 4 : More Commands

`Tree` show directroy as tree 

```bash
root@G580:/var/log/mysql# tree
.
├── error.log
├── error.log.1.gz
├── nothing
│   ├── nothing1
│   ├── nothing2
│   ├── nothing3
│   ├── nothing4
│   └── nothing5
└── testing
    ├── file1
    ├── file2
    ├── file3
    ├── file4
    └── file5

2 directories, 12 files
```

`mkdir`  : Make Directory 

```bash
mkdir new_dir # make new dir called new_dir 
mkdir newfile{1..4} # make new 4-directorys called new_dir1,new_dir2_newdir_3,new_dir4
mkdir temp/dir # if temp not already directory exists will get error to fix this use -p 
# if perant dir not even exist create him and same with chiled who's perant to who's under him 
# like temp is perant to dir and dir is child for temp but perant for testing and so on  
mkdir -p temp/dir/testing/nothing/
```

`cp`  : copy 

```bash
cp source desctnation
cp /file/ /backup_file/
# when trying to use cp with directorys like make backup from /etc/
# use 
cp -R /etc/ /backup/
# if you wanna copy dir with special name 
cp -r /etc/ /backup/new_etc
```

`cat` : reading text files

```bash
root@G580:~# cat msg 
This is msg file and you can read me using cat msg :) .
```

`mv` it's `cp` but cp don't delete source

```bash
root@G580:~/labs# touch file{1..4}
root@G580:~/labs# mkdir back_up
root@G580:~/labs# tree
.
├── back_up
├── file1
├── file2
├── file3
└── file4
1 directory, 4 files
root@G580:~/labs# mv file* back_up/
root@G580:~/labs# tree
.
└── back_up
    ├── file1
    ├── file2
    ├── file3
    └── file4
1 directory, 4 files
```

---

## Day 5 : Basics Administration

#### info :

> **Normal users** There ID-Range : Starts From 1000
> 
> **root** His ID only 0
> 
> **Services** There ID-Range : From 1 To 999

- > all users saved in etc/passwd

- ```bash
  cat /etc/passwd
  xy:x:1000:1000:xy,,,:/home/xy:/bin/bash
  mysql:x:132:139:MySQL Server,,,:/nonexistent:/bin/false
  geoclue:x:133:140::/var/lib/geoclue:/usr/sbin/nologin
  ```

### Basics Commands with users

#### `useradd` :

> users info saved into `/etc/passwd`

```bash
# Basics user addition
useradd web_adm_usr
# after adding group and want to add new user in this group 
useradd -g WebAD web_adm_usr # web_adm_usr will be in WebAD group
# WebAD group will be The Primary Group for web_adm_usr
userdel web_adm_usr # will remove user but leave his dir
userdel web_adm_usr -r # remove everything for this user 
```

#### `groupadd` :

> groups info saved into `/etc/group`

```bash
groupadd DCAdmins
groupadd NetwrokAdmins
groupadd DBadmins
groupadd WebAD
```

#### `usermod` & `groupmod` to edit user & groups

```bash
# u have been added web_adm_usr
# so to add him to more then one group "Secondary Groups"
# use -G to add only one secondary group 
$: useradd web_adm_usr
$: id web_adm_ur
# userID                Primary Group ID(name)  Seconday Groups
uid=1001(web_adm_usr)   gid=1005(web_adm_usr)   groups=1005(web_adm_usr)
# when you use only -G he add update old seconday Group by new group and add both
$: usermod -G DCADM web_adm_usr
$: id web_adm_usr
uid=1001(web_adm_usr) gid=1005(web_adm_usr) groups=1005(web_adm_usr),1002(DCADM)
$: usermod -G NETAD web_adm_usr
$: id web_adm_usr
uid=1001(web_adm_usr) gid=1005(web_adm_usr) groups=1005(web_adm_usr),1003(NETAD)
#if you looked at secondary Group you will see it's replaced old one by new one
# to Fix this use -a with -G 
$: usermod -aG DCADM web_adm_usr
$: id web_adm_usr
# added more then one in secondary group
uid=1001(web_adm_usr) gid=1005(web_adm_usr) groups=1005(web_adm_usr),1002(DCADM),1003(NETAD)
# to replace old primary group use -g in usermod
$: usermod -g DCADM web_adm_usr
$: id web_adm_usr
uid=1001(web_adm_usr) gid=1002(DCADM) groups=1002(DCADM),1003(NETAD)
# so -g for Primary -G for Seconday *u can use -a with -g* you only have a one primary group


# renameing groups
groupmod -n "WEB_DEV" web_developers
```

#### reading `etc/passwd`

```bash
$: cat /etc/passwd
web_adm_usr:x:1001:1002::/home/web_adm_usr:/bin/sh
web_adm_usr : # user name
x: # is password but to more secure added x 
# and hash of passwords will be in /etc/shadow
#like my xy user password is $y$j9T$7r1EbrB9cAiFRIMAgkoI3.$DzvR9nLYCJGRK9oZa0iUWHAEhnhFeSqMApeUF51ExVC:19714:0:99999:7:::
# it's 123 :) and hash algorithms is SHA
1001 : # it's usrID 
1002 : # it's Primary group ID 
# between 1001 , 1002 it's a desription for user called GECOS Field  
# to add description use useradd -c or usermod -c 
usermod -c "this a web admin user" web_adm_usr 
$: tail  -n 1 /etc/passwd
web_adm_usr:x:1001:1003:this a web admin user:/home/web_adm_usr:/bin/sh
/home/web_adm_usr : # it's a home directory for this user
/bin/sh : # it's user shell path 
```

> users passwords will be in /etc/shadow
> 
> and groups passwords in /etc/gshadow 

### Permissions

```bash
We Have 3 permissions on any File 
1. User OWNER => RWX
2. Group OWNER => RWX
3. Other => RWX
and 1st 3 bits For user & 2nd 3 bits For Group & 3rd 3 Bits For Other & First bit For File Type
---------------------------------------------------------
-rw-r--r--
R = Read
W = Write 
X = Execute
- = File Type (- = normal File , d = Directory , b = Block Device , c = Char Device , l = Link File )
# char device like keyboard 
$: ll /dev/tty1 
crw--w---- 1 root tty 4, 1 Jan 24 08:19 /dev/tty1
# blok device like HardDisk or USB or floppy Disk
$: ll /dev/sda
brw-rw---- 1 root disk 8, 0 Jan 24 08:19 /dev/sda
Reading Permissions :
-rw-r--r--
    - File Type = normal File 
    rw- = user  can Read & Write on this File 
    r-- = Group can Read Only This File
    r-- = Other have same Group Permission 

Reading Permissions 
$: ls -la # some Linux Distro adding ll and do the same job of ls -la 
# to add ll Manual use alial 
$: alias ll="ls -la"
$: ll
total 8
drwxr-xr-x 2 root root 4096 Jan 23 16:31 .
drwxr-xr-x 3 root root 4096 Jan 23 16:31 ..
-rw-r--r-- 1 root root    0 Jan 23 16:31 file1
-rw-r--r-- 1 root root    0 Jan 23 16:31 file2
-rw-r--r-- 1 root root    0 Jan 23 16:31 file3
-rw-r--r-- 1 root root    0 Jan 23 16:31 file4

# Explaining
-rw-r--r-- 1 root root    0 Jan 23 16:31 file4
0. drwxr #File Type 
1.-rw-r--r-- # Permissions Read Write Execute
2. 1 # Link Counter
3. root # USER  OWNER
4. root # Group OWNER
5. 0 # file Size
6. Jan 23 16:31 # Last Access not Modifition Time
7. File4 # file name
```

#### Edit Permissions

```bash
$: ll file1 
-rw-r--r-- 1 root root 0 Jan 23 16:31 file1
$: chmod o+wx file1 
$: ll file1 
-rw-r--rwx 1 root root 0 Jan 23 16:31 file1*
$: chmod {a or }{+,-}{w,r,x} file1 # will remove x permission from all of them 
chmod a-x file1 # file1 will be file without exec permission
chmod ugo+wr,o-wrx # owner & group will get wr permissions and o will be null
# to apply permissions in all things in speical dir use -R 
$: chmod go-rwx
$: ll
drwx------ 2 root root 4096 Jan 24 10:42 DBFiles/
$: ll DBFiles/
-rw-r--r-- 1 root root    0 Jan 24 10:42 file1.db
-rw-r--r-- 1 root root    0 Jan 24 10:42 file2.db
-rw-r--r-- 1 root root    0 Jan 24 10:42 file3.db
-rw-r--r-- 1 root root    0 Jan 24 10:42 file4.db
# Directory got removed GO permissions but File who's inside This Dir not got the same permissions 
# to make all dir and the file inside this dir use -R
$: chmod -R go-wrx,u+rwx DBFiles/
$: ll
total 12
drwxr-xr-x 3 root root 4096 Jan 24 10:42 ./
drwxr-xr-x 3 root root 4096 Jan 23 16:31 ../
drwx------ 2 root root 4096 Jan 24 10:42 DBFiles/
$: ll DBFiles/
total 8
drwx------ 2 root root 4096 Jan 24 10:42 ./
drwxr-xr-x 3 root root 4096 Jan 24 10:42 ../
-rwx------ 1 root root    0 Jan 24 10:42 file1.db*
-rwx------ 1 root root    0 Jan 24 10:42 file2.db*
-rwx------ 1 root root    0 Jan 24 10:42 file3.db*
-rwx------ 1 root root    0 Jan 24 10:42 file4.db* 
```

#### file Permissions

| Symbol | means                                          |
|:------:|:----------------------------------------------:|
| read   | View                                           |
| write  | edit , del , overload , any kind under editing |
| exec   | run file                                       |

#### Direcotry Permissions

| Symbol | means                                        |
|:------:|:--------------------------------------------:|
| read   | ls this dir                                  |
| write  | add , Remove , Delete Directory              |
| exec   | cd dir , ls -l dir _-l :Long Listing Format_ |

#### `chown` : Change Ownership on files or Dir

```bash
chown username:group {filename,dir}
$: ll
drwx------ 2 root root 4096 Jan 24 10:42 DBFiles/
$: chown web_adm_usr:WEBAD DBFiles/
$: ll
drwx------ 2 web_adm_usr WEBAD 4096 Jan 24 10:42 DBFiles/
# changeing group only
chown :WEBAD DBFiles/
```

### Permission $Kind$

1. Symbolic Method 

2. Numeric method 

#### Symbol :

user owner =  $u$

group owner =  $g$

other = $o$ 

#### Numeric :

| Syntax | number |
|:------:|:------:|
| r      | 4      |
| w      | 2      |
| x      | 1      |

> U,G,O Every one of them have this 3 Numbers 4,2,1 

```bash
chmod 775 file1
# means user=rwx
# means Group=rwx
# means Other=rx
$: touch file1 
$: chmod 775 file1 
$: ll
total 12
-rwxrwxr-x 1 root root    0 Jan 24 11:48 file1*
```

## Day 6 :  Redicetion

### Descriptor

| symbol | number |
|:------:|:------:|
| input  | 0      |
| output | 1      |
| error  | 2      |

### output redirection

```bash
ls > ls_out # if ls_out not exists will be created and save output from ls
ls askdbasd 2> ls_out # 2> for redirect errors
*> == 1> *
ls File dir_not_exits >resuilt 2>errors
ls File dir_not_exits 2&>>all_Resuilt
# when using > he overload file
# but >> same old and add new 
```

### input

```bash
# defualt input is null 
cat < file == cat file
*reading and adding using cat*
cat <<EOT>> new_file
# new file 
# adding new file 
# anything new 
# EOT
# cat << ; for adding on old content not overloading 
# EOT just text to tell bash when see EOT stop reading 
# after stop reading will redirect using EOT>> new_file
 cat <<addedby me >> file
```

> explaned this commands
> 
> 1. more : seeing file + auto close 
> 
> 2. less : seeing file + manual close
> 
> 3. | between 2 commands
> 
> 4. tee with ls & | 
>    
>    1. ls | tee -a resuilt.txt     *-t for don't overloading*
>       
>       _this command will return resuilt into screen and save output into resuilt_
> 
> 5. w : whois login + some info 
> 
> 6. who : whois login into system and running 
> 
> 7. whoami or who am i 
> 
> 8. whatis {ls , pwd , chmod , chown}
> 
> 9. whereis {{ls , pwd , chmod , chown} return binary bath
> 
> 10. last 

---

## Day 7 & Day 8

> MBR <Master Boot Record>
> 
> Have 3 Spaces :
> 
> Partition Table __For Knowing The Start and The End of this partitions & disk__
> 
> **Partition Table is removed that's mean you hard Disk got formated**
> 
> **FILE SYSTEMs**  : `NTFS` , `EXT` , `ETX32` and so on see [There](en.wikipedia.org/wiki/File_system) For **More**
> 
> For Every Partition we have **Inode Table** and  it's normal table store info of anything will be stored in this partition 
> 
> 1 Parition Table it's store strart x to end y and Block number x+15 have data with permission RWX for user and RW for other and - - - For Group  and more info for any thing will be stored in this blcoks  "Metadata"
> 
> ---
> 
> Let's Collect this 
> 
> We have MBR and MBR Have Partition Table for Every Partition to know The Start And The End for this Partitions  and every Partition Table Have his own speically Inode Table And Inode Table have all informatoin in every Sector Or Block whatever in this space inside Partition 
> 
> ex : HHD = 400G 
> 
> 4 Partitions 
> 
> MBR Will store From 0 to 100 this partition 1 and so on for partition 4
> 
> and For Every PartitionX have Inode Table and this table Store all blocks From X to x+100
> 
> __If Inode Table To corrupted__ This Partition only got stoped and don't work anymore but if you formated it Kernel Will Create New Partition Table and send it to MBR and remove Corrupted __INODE TABLE__ and add new **INODE TABLE** 

### Seeing Partition Table

```bash
$: fdisk -l /dev/sda
Disk /dev/sda: 465.76 GiB, 500107862016 bytes, 976773168 sectors
Disk model: ST500LT012-9WS14
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 4096 bytes
I/O size (minimum/optimal): 4096 bytes / 4096 bytes
Disklabel type: gpt
Disk identifier: B0CFC205-CDE7-47F1-9670-7F1A64BA0BB2

Device         Start       End   Sectors   Size Type
/dev/sda1       2048   9764863   9762816   4.7G EFI System
/dev/sda2    9764864  19529727   9764864   4.7G BIOS boot
/dev/sda3   19529728  39061503  19531776   9.3G Linux swap
/dev/sda4   39061504 332029951 292968448 139.7G Linux filesystem
/dev/sda5  332032000 490639359 158607360  75.6G Linux filesystem
/dev/sda6  490639360 976773119 486133760 231.8G Microsoft basic data
# fdisk -list device 
return 
    1. device or partition name "in Linux /dev/sdX"
    2. Start and of this partition
    3. Sector 
    4. size this of all partition not what i used in this partition
    5. File System Type     
```

### Seaing INODE-Number

```bash
$: ls -li 
total 4
131090 drwxr-xr-x 3 root root 4096 Jan 24 11:48 back_up
# First Table is INODE-NUMBER and other we know what they are
```

> I-NODE != based on size of file  let's see what' i wanna tell You

```bash
$: df -hi 
# df -human-readable  -inode-number 
Filesystem     Inodes IUsed IFree IUse% Mounted on
/dev/sda4        8.8M  439K  8.4M    5% /
# now The I-Node in my / partition in /dev/sda4 
# This Partition It's Size is 8.8M and i only used 439K of 8.8M 
# so now only 439K used 95% of my space that's means 
# inode number don't use every Block and gave this block his own inode number
# no that mean you have large files and this files used space as well
# and you have free inode ex you can add Large number of empty files or small files in system  
$: df -h 
/dev/sda4       137G  123G  7.1G  95% /
```

### Real DEMO

```bash
# Let's see First inode table on / whois in /dev/sda4
$: df -i | grep "/dev/sda4"
/dev/sda4      9158656 448903 8709753    5% /
# we will use dd to write into file and make this files takes 2G
$: dd if=/dev/zero of=testing.inode bs=1M count=2024 status=progress
2090860544 bytes (2.1 GB, 1.9 GiB) copied, 19 s, 110 MB/s
2024+0 records in
2024+0 records out
2122317824 bytes (2.1 GB, 2.0 GiB) copied, 23.2707 s, 91.2 MB/s
# we write 2024MB into file called test.incode
# let's see inode table new using df -i 
$: df -i | grep "/dev/sda4"
/dev/sda4      9158656 448904 8709752    5% /
# look Here he used only 1 inode number to point to this file
# The i-node Table don't care about size of file
# he's only cares about number of files will use number of nodes 
# for more info 
$: touch file{1..50}
$: df -i | grep "/dev/sda4"
/dev/sda4      9158656 448954 8709702    5% /
# from 448904 to 448954 that exactly number of files we got created them 
# using touch and so on with every files and directory you working with them
```

### Soft Links & Hard Link

---

#### Soft Link

>  soft link and hard link it's like shortcut in Windows 
> 
> 

#### Demo :  Hard Link

```bash
------------------------------- Hard Link -------------------------------
df -i | grep "/dev/sda4" # for seaing inode number before adding file
/dev/sda4      9158656 446866 8711790    5% /
$: touch file1
$:  df -i | grep "/dev/sda4"
/dev/sda4      9158656 446867 8711789    5% /
# inode number from 446866 to 446867 that's mean we used inode number for file 
$: ls -li # show i node number of file1 before hard linking  
total 0
131077 -rw-r--r-- 1 root root 0 Jan 25 12:03 file1
$: ln file1 file2
$: ls -li 
total 0
131077 -rw-r--r-- 2 root root 0 Jan 25 12:03 file1
131077 -rw-r--r-- 2 root root 0 Jan 25 12:03 file2 
# They Have The same inode number in "hard link"
while rm -rf file1 , file2 still have access to this data why ?
# while removing any file OS don't remove there data
# it's only delete the falg on this inodes and set them as free 
# so when we created 2 files point to the same file OS removed lable1 but still see lable2 on file2
# when removing file2 data still in sys but can't access it 
# someting like pointer in c++ when creaing new memory allocator you should delete it after done work    
```

#### Demo : Soft Link

```bash
------------------------------- Soft Link -------------------------------
$: ln -s file1 file2 
$: ll -i
131077 -rw-r--r--  1 root root     10 Jan 25 12:10 fil1
131085 lrwxrwxrwx  1 root root      4 Jan 25 12:14 file2 -> fil1
# every file have how own inode number 
# you can remove child links but when remove perant link child link don't know where they will go 
$: rm -rf fil1  # will remove perant link so when open file2 
$: cat file2 
cat: file2: No such file or directory
# while removing child link 
$: ln -s main_soft child
$: ll -i 
total 140
131084 drwxr-xr-x  2 root root 131072 Jan 25 12:22 ./
131073 drwx------ 10 root root   4096 Jan 25 12:10 ../
131085 lrwxrwxrwx  1 root root      9 Jan 25 12:22 child -> main_soft
131077 -rw-r--r--  1 root root     11 Jan 25 12:21 main_soft
# main_soft & child have diffrent inode number 
$: echo "soft link" > main_soft
$: ll -i main_soft child 
131085 lrwxrwxrwx 1 root root  9 Jan 25 12:26 child -> main_soft
131077 -rw-r--r-- 1 root root 10 Jan 25 12:24 main_soft
$: cat child main_soft 
soft link 
soft link
$: echo "adding comment" >> child 
$: cat child main_soft 
soft link
adding comment
soft link
adding comment
$: rm -rf child 
$: ll -i main_soft child 
ls: cannot access 'child': No such file or directory
131077 -rw-r--r-- 1 root root 25 Jan 25 12:26 main_soft
$: cat main_soft 
soft link
adding comment
# still have main_soft content but child got removed
```

> bin and system bin are Soft link for /usr/bin

```bash
ll -i /
total 157292
      2 drwxr-xr-x  20 root root      4096 Jan 23 16:24 ./
      2 drwxr-xr-x  20 root root      4096 Jan 23 16:24 ../
     12 lrwxrwxrwx   1 root root         7 Dec 23 11:16 bin -> usr/bin/
7340033 drwxr-xr-x   4 root root      4096 Dec 25 06:43 boot/
2621441 drwxrwr-x   2 root root      4096 Dec 23 11:22 cdrom/
   3010 -rw-------   1 root root 197763072 Dec 29 22:22 core.831
      1 drwxr-xr-x  21 root root      5060 Jan 25 08:03 dev/
 786433 drwxr-xr-x 170 root root     12288 Jan 24 20:48 etc/
2359297 drwxr-xr-x   3 root root      4096 Dec 23 11:23 home/
     13 lrwxrwxrwx   1 root root         7 Dec 23 11:16 lib -> usr/lib/
     14 lrwxrwxrwx   1 root root         9 Dec 23 11:16 lib32 -> usr/lib32/
     15 lrwxrwxrwx   1 root root         9 Dec 23 11:16 lib64 -> usr/lib64/
     16 lrwxrwxrwx   1 root root        10 Dec 23 11:16 libx32 -> usr/libx32/
     11 drwx------   2 root root     16384 Dec 23 11:16 lost+found/
6029313 drwxr-xr-x   3 root root      4096 Dec 23 11:31 media/
1835009 drwxr-xr-x   3 root root      4096 Jan 19 23:45 mnt/
6815745 drwxr-xr-x   3 root root      4096 Jan  6 09:36 opt/
      1 dr-xr-xr-x 311 root root         0 Jan 25 08:02 proc/
 131073 drwx------  10 root root      4096 Jan 25 12:10 root/
      1 drwxr-xr-x  43 root root      1200 Jan 25 11:41 run/
     17 lrwxrwxrwx   1 root root         8 Dec 23 11:16 sbin -> usr/sbin/
3407873 drwxr-xr-x  30 root root      4096 Jan 22 14:45 snap/
 262145 drwxr-xr-x   2 root root      4096 Aug  9  2022 srv/
      1 dr-xr-xr-x  13 root root         0 Jan 25 08:02 sys/
1048577 drwxrwxrwt  16 root root      4096 Jan 25 12:09 tmp/
3538945 drwxr-xr-x  16 root root      4096 Dec 23 12:43 usr/
1179649 drwxr-xr-x  15 root root      4096 Jan  3 21:12 var/
--------------------------------------------------------------------------
$: ll -i /lib
13 lrwxrwxrwx 1 root root 7 Dec 23 11:16 /lib -> usr/lib/
$: ll -i /usr/ | grep lib/
3538949 drwxr-xr-x 131 root root  4096 Jan 20 21:18 lib/
# /lib and /usr/lib are soft link
# when remove /lib whois under / nothing gonna happen .  
```

> - hard link not working with directorys but soft works 
> 
> - ln mydir/ hardlink != ls -s mydir/ softlink 
> 
> - *while using soft link* you should use absolute path
