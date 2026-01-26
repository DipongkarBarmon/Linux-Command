Linux for Developers

1. How does the internet work? what are server?




  
//How a Website Request Works (Step-by-Step)

Example: You type
https://example.com

Step 1: DNS(Domain Name Server) Lookup 

The browser asks: “What is the IP address of example.com?”

DNS converts the domain name to an IP address (e.g., 93.184.216.34)

Step 2: TCP Connection

Your browser creates a connection to the server using TCP

Step 3: HTTP Request

Browser sends an HTTP request:

GET / HTTP/1.1
Host: example.com

Step 4: Server Processing

Server receives request

Processes it (maybe queries database)

Prepares a response

Step 5: HTTP Response
HTTP/1.1 200 OK
Content-Type: text/html

Step 6: Rendering

Browser renders the page on your screen

// What Are IP Addresses?

An IP address uniquely identifies a device on a network.

IPv4: 192.168.1.1

IPv6: 2001:db8::1

Servers usually have static IP addresses so clients can always find them.




//What Is HTTP / HTTPS?

HTTP: Protocol for transferring web data

HTTPS: HTTP + encryption (SSL/TLS)

HTTPS ensures:

Data privacy

Data integrity

Server authenticity






How TCP(Transmission Control Protocol) Works (Step-by-Step)

1. Connection Establishment (3-Way Handshake)

Before sending data, TCP establishes a connection:

SYN:
 client->server

“I want to connect with you. Are you available?”

SYN-ACK (Synchronize + Acknowledge): 
Server->client  
“Yes, I am availabl3. Connection Termination

When communication ends:

FIN and ACK packets close the connection cleanly  e, and I received your request.”

ACK:
 Client->server: 
 “Okay, I received your reply. Let’s start sending data.”

Connection is now established.

2. Data Transfer

Data is split into segments

Each segment has a sequence number

Receiver sends ACKs for received data

Missing segments are retransmitted

3. Connection Termination

When communication ends:

FIN and ACK packets close the connection cleanly






Qusetion 2: Difference between web server and application server?

Web Server:

Purpose: A web server handles HTTP requests and serves static content (files) such as HTML, CSS, images, and videos.

Main Work:

Receives browser requests

Sends static files

Forwards dynamic requests to application server

Examples: Apache, Nginx

Functionality: Handles HTTP requests, delivers files

Application Server:

Purpose: An application server runs business logic and generates dynamic content (data from databases, APIs, authentication, etc.).

Main Work:

Processes application logic

Connects to databases

Returns dynamic responses (JSON, HTML)


Examples: Tomcat, Node.js, Django ,JBoss, Spring Boot

Functionality: Executes application code, processes requests

Difference:

Web servers serve static content

Application servers run dynamic applications

They often work together (web server handles static content, application server handles dynamic content)




Qusetion 3: What is the difference between HTTP and HTTPS?

HTTP (Hypertext Transfer Protocol):

Port: 80

Security: No encryption

Data: Sent in plain text

HTTPS (HTTP Secure):

Port: 443

Security: Uses SSL/TLS encryption

Data: Encrypted during transmission

HTTPS ensures:

Privacy (data cannot be read by third parties)

Integrity (data cannot be altered)

Authentication (verifies server identity)



Qusetion 4: What is the difference between TCP and UDP?

TCP (Transmission Control Protocol):

Connection-oriented

Reliable (acknowledges data receipt)

Ordered delivery

Error checking

Flow control

UDP (User Datagram Protocol):

Connectionless

Unreliable (does not guarantee delivery)

No ordering

No error checking

No flow control

TCP is used for web browsing, email, file transfers

UDP is used for video streaming, online gaming, DNS




Application type
 1.Standalone type
 2. web application

what is a standalone apps?
A standalone application is a software program that runs independently on a user’s device and does not require an internet connection or another system to function.

Examples of Standalone Applications

Calculator
Notepad
Microsoft Word (desktop version)
Paint
VLC Media Player
Offline games

what are a web applications?
A web application is a software application that runs on a web server and is accessed through a web browser using the internet.
Examples of Web Applications
Gmail
Facebook
YouTube
Online banking systems
E-commerce websites (Amazon)
Online forms and dashboards



90% application linux(operating system)
linux -> open source operating system
unix -> not open source need to buy example macOS

unix parent of linux



software remote location  server tools?
hese are tools used to access, manage, monitor, or control servers remotely (servers located in another physical location).

Remote Access Tools

Used to log in to a remote server.

Tool	Purpose
SSH	-Secure command-line access (Linux servers)
PuTTY -	SSH client for Windows
Remote Desktop (RDP) -	GUI access to Windows servers
VNC-	Remote desktop access (cross-platform)

Example:
ssh user@server_ip




what are the karnal,Bootloader and shell?

1️⃣ Kernel

Definition:
The kernel is the core part of an operating system. It manages the hardware (CPU, memory, devices) and provides services to software programs.

Key Points:

Acts as a bridge between hardware and applications

Manages processes, memory, files, and devices

Runs in protected mode

Can be monolithic (Linux) or microkernel (Minix)

Example:

Linux kernel

Windows NT kernel

Analogy:

Kernel = Brain of the computer. It tells hardware what to do when software requests it.

2️⃣ Bootloader

Definition:
A bootloader is a small program that loads the operating system into memory when the computer starts.

Key Points:

Runs before the OS

Initializes hardware

Loads the kernel into memory

Lets you choose between multiple OS (dual boot)

Example:

GRUB (Linux bootloader)

Windows Boot Manager

Analogy:

Bootloader = Starter motor of a car. It starts the engine (OS) when you turn the key.

3️⃣ Shell

Definition:
A shell is a program that takes user commands and communicates them to the operating system (kernel).

Key Points:

Can be command-line (CLI) or graphical (GUI)

Provides an interface to run programs, scripts, and manage files

Shell itself is not the OS but interacts with it

Example:

Bash, Zsh (Linux)

Command Prompt, PowerShell (Windows)

Analogy:

Shell = Interpreter or messenger. You tell it what you want, it tells the kernel to do it.



linux system architecture :
hardware<-kanel<-shell<-Applications/utillities


***linux command***

ls -> list 

ls -l -> list with creation time

pwd -> show current directory

touch <file_Name formate .txt or any thing> -> create a file

mkdir <folder_name> -> create a folder

rm <file_name> ->  delete or remove 

rm -r <folder_name> -> delete folder

flag -r -> recurcively

rmdir <folder_name> -> delete folder

date -> it show today date

cal -> it show calender

touch -> it create a file

echo <message> -> it print the 

echo <message> > <file_name> -> it create a file and write the message in it

echo <message> >> <file_name> -> it append the message in the file

cat <file_name> -> it show the content of the file  

cat <file_name> <file_name> -> it show the content of the file and file

head <file_name> -> it show the first 10 line of the file

tail <file_name> -> it show the last 10 line of the file

less <file_name> -> it show the content of the file and we can scroll up and down

more <file_name> -> it show the content of the file and we can scroll up and down 


cp <file_name> <new_file_name> -> it copy the file

cp -r <folder_name> <new_folder_name> -> it copy the folder

cp <file_name> <folder_name> -> it copy the file to the folder

cp <file_name> <folder_name>/<file_name> -> it copy the file to the folder 
with new name

cp <file_name> <folder_name>/<new_file_name> -> it copy the file to the folder 
with new name

cp <file_name> <folder_name>/<file_name> -> it copy the file to the folder 
with new name

cp <folder_name>/<file_name>  <folder_name> -> it copy the file to the folder 



mv <file_name> <new_file_name> -> it rename the file

mv <file_name> <folder_name> -> it move the file to the folder
mv <file_name> <folder_name>/<file_name> -> it move the file to the folder 
with new name

mv <file_name> <folder_name>/<new_file_name> -> it move the file to the folder 
with new name 
mv <folder_name>/<file_name>  <folder_name> -> it move the file to the folder 
mv <folder_name>/<file_name>  <folder_name>/<new_file_name> -> it move the file to the folder 
with new name


wc <file_name> -> it show the word count of the file (line , word , byte)


soft link -> it create a link of the file

ln -s <file_name> <link_name> -> it create a soft link of the file

ls -ltr -> it show the file and folder in the current directo

hard link -> it create a link of the file

ln <file_name> <link_name> -> it create a hard link of the file 


cut -d <delimiter> -f <field_number> <file_name> -> it cut the field from the file
cut -d <delimiter> -f <field_number> -f <field_number> <file_name> -> it cut the field from the file

cut -d <delimiter> -f <field_number> -f <field_number> <file_name> > <new_file_name> -> it cut the field from the file and save in new file

cut -d <delimiter> -f <field_number> -f <field_number> <file_name> >> <new_file_name> -> it cut the field from the file and append in new file

cut -d <delimiter> -f <field_number> -f <field_number> <file_name> | cut -d <delimiter> -f <field_number> -f <field_number> > <new_file_name> -> it cut the field from the file and save in new file



cut -b <start_byte>-<end_byte> <file_name> -> it cut the byte from the file

cut -b <start_byte>-<end_byte> <file_name> > <new_file_name> -> it cut the byte from the file and save in new file

cut -b <start_byte>-<end_byte> <file_name> >> <new_file_name> -> it cut the byte from the file and append in new file



sort <file_name> -> it sort the file

sort -r <file_name> -> it sort the file in reverse order

sort -n <file_name> -> it sort the file in numerical order

sort -u <file_name> -> it sort the file and remove the duplicate line

sort -k <field_number> <file_name> -> it sort the file on the basis of field number

sort -k <field_number> -r <file_name> -> it sort the file on the basis of field number in reverse order

sort -k <field_number> -n <file_name> -> it sort the file on the basis of field number in numerical order

sort -k <field_number> -u <file_name> -> it sort the file on the basis of field number and remove the duplicate line

sort -k <field_number> -k <field_number> <file_name> -> it sort the file on the basis of field number and field number

sort -k <field_number> -k <field_number> -r <file_name> -> it sort the file on the basis of field number and field number in reverse order

sort -k <field_number> -k <field_number> -n <file> -> it sort the file on the basis of field number and field number in numerical order

sort -k <field_number> -k <field_number> -u <file_name> -> it sort the file on the basis of field number and field number and remove the duplicate line




tee -> it is used to write the output of the command in the file and also in the terminal

echo "Hello" | tee hello.txt

echo "Hello" | tee -a hello.txt -> it append the output of the command in the file 


diff <file_name1> <file_name2> -> it show the diffence between them


diff -y <file_name1> <file_name2> -> it show the diffence between them in side by side format


df -> it show the disk space

df -h -> it show the disk space in human readable format

df -h / -> it show the disk space of root directory in human readable format

du -> it show the disk space of current directory

du -h -> it show the disk space of current directory in human readable format

du -h / -> it show the disk space of root directory in human readable format

du . -> 

ls -a -> it show all directory with hiden directory

ps -> ps stands for Process Status. It is used to display information about running processes in a Linux/Unix system.

top -> top is a real-time process monitoring command in Linux.
It continuously displays running processes, sorted by resource usage (CPU by default).


free -> it show about ram

free -h -> it show about ram in human readable format

free -m -> it show about ram in MB
free -g -> it show about ram in GB
free -t -> it show about ram in total
free -t -h -> it show about ram in total in human readable format


nohup -> it is used to run the command in the background and it will not stop even if the terminal is closed

nohup <command> & -> it is used to run the command in the background and it will not stop even if the terminal is closed

nohup <command> > <file_name> & -> it is used to run the command in the background and it will not stop even if the terminal is closed and it will store the output in the file

 

vmstat -> it is used to show the virtual memory statistics




kill ->kill is a Linux command used to send a signal to a process, usually to terminate (stop) a running process.

Basic syntax
kill [signal] <PID>

1️⃣ Normal process termination (recommended)
kill <PID>
or 
kill -15 <PID>
Meaning

Sends SIGTERM (15)

Allows the process to clean up resources before exiting

2️⃣ Force kill (when process does not stop)
kill -9 <PID>

Meaning

Sends SIGKILL (9)

Process is immediately stopped

No cleanup (use carefully)

3️⃣ Kill using signal name
kill -SIGTERM <PID>
kill -SIGKILL <PID>

4️⃣ Find PID and kill process
ps -ef | grep nginx
kill 2456

5️⃣ Kill multiple processes
kill 1234 1235 1236

6️⃣ Kill all processes by name (killall)
killall firefox

7️⃣ Kill from top

Steps:

Run top

Press k

Enter PID

Press Enter





pwd -> it is used to show the current working directory

show : /home/dipongkar

cd -> it is used to change the directory

show : cd /home/dipongkar

ls -> it is used to list the files and directories

show : ls

ls -l -> it is used to list the files and directories in detail

show : ls -l

ls -a -> it is used to list the hidden files and directories

show : ls -a

ls -la -> it is used to list the hidden files and directories in detail

show : ls -la

ls -lh -> it is used to list the files and directories in human readable format

show : ls -lh

ls -lhS -> it is used to list the files and directories in human readable format and sorted by size

show : ls -lhS

ls -lht -> it is used to list the files and directories in human readable format and sorted by time

show : ls -lht

ls -lhSrt -> it is used to list the files and directories in human readable format and sorted by size in

 


1. System Level Command

uname -> it is used to show the system information which system is running exmaple linux

uname -a -> it is used to show the system information in detail

show : Linux Dip 6.14.0-37-generic #37~24.04.1-Ubuntu SMP PREEMPT_DYNAMIC Thu Nov 20 10:25:38 UTC 2 x86_64 x86_64 x86_64 GNU/Linux

Meaning of each part
Part	                               Explanation
Linux	                            Kernel name (Linux kernel)
Dip                              	Hostname (computer name)
6.14.0-37-generic	                Kernel version
#37~24.04.1-Ubuntu	              Kernel build number and Ubuntu release
SMP	                              Symmetric Multi-Processing (supports        multiple CPUs/cores)
PREEMPT_DYNAMIC	                  Kernel preemption model (better responsiveness)
Thu Nov 20 10:25:38 UTC 2024	    Kernel build date and time
x86_64	                          CPU architecture (64-bit)
x86_64	                          Hardware platform
x86_64	                          Processor type
GNU/Linux	                        Operating system (GNU tools + Linux kernel)


uname -r -> it is used to show the kernel version

uname -s   # Kernel name
uname -n   # Hostname
uname -r   # Kernel version
uname -m   # Architecture
uname -o   # OS type

uptime -> it show how many time system is running 



who -> who is a Linux command used to show who is currently logged in to the system.

show :
dipongkar seat0        2026-01-26 08:59 (login screen)
dipongkar tty2         2026-01-26 08:59 (tty2)

Column meaning (from who)
Column	                        Meaning
dipongkar	                    Username
seat0 / tty2	                Login terminal
2026-01-26 08:59	            Login date and time
(login screen) / (tty2)	      Login source


whoami -> it is used to show the current user name
show : dipongkar

which -> it is used to show the path of the command

show : /usr/bin/which


id -> show user id (uid) group id (gid) groups=....

show : uid=1000(dipongkar) gid=1000(dipongkar) groups=1000(dipongkar),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),122(lpadmin),138(lxd),139(sambashare)

shutdown -> it is used to shutdown the system

shutdown -r -> it is used to restart the system

shutdown -c -> it is used to cancel the shutdown or restart command

shutdown -h -> it is used to shutdown the system

shutdown -h now -> it is used to shutdown the system immediately

shutdown -h 10 -> it is used to shutdown the system after 10 minutes

if not working(because not root user) then use sudo shutdown -c

sudo shutdown 


ctrl+r -> it is used to search the command in the history reverse direction
ctrl+b -> it is used to search the command in the history forward direction

history -> it is used to show the history of the command

ctrl+c -> it is used to stop the command

ctrl+z -> it is used to pause the command

ctrl+d -> it is used to exit the terminal


apt -> it is used to install the package

apt install <package_name> -> it is used to install the package

apt remove <package_name> -> it is used to remove the package

apt update -> it is used to update the package list

apt upgrade -> it is used to upgrade the package

apt search <package_name> -> it is used to search the package

apt show <package_name> -> it is used to show the package details

apt list -> it is used to list the package

apt list --installed -> it is used to list the installed package

apt list --upgradable -> it is used to list the upgradable package

apt list --all-versions -> it is used to list the all versions of the package

apt list --installed --upgradable -> it is used to list the installed and upgradable package

apt list --installed --upgradable --all-versions -> it is used to list the installed, upgradable and all versions of the package

apt list --installed --upgradable --all-versions | grep <package_name> -> it is used to list the installed, upgradable and all versions of the package and grep the package name

apt list --installed --





User & Group Management command

we need to add "sudo" for these commands at first
like sudo useradd -m ... 

useradd -> it is used to add the user

useradd -m <username> -> it is used to add the user with home directory

useradd -m -s /bin/bash <username> -> it is used to add the user with home directory and bash shell

useradd -m -s /bin/bash -G sudo <username> -> it is used to add the user with home directory, bash shell and sudo group

useradd -m -s /bin/bash -G sudo -p $(openssl passwd -1 <password>) <username> -> it is used to add the user with home directory, bash shell, sudo group and password

useradd -m -s /bin/bash -G sudo -p $(openssl passwd -1 <password>) -e <date> <username> -> it is used to add the user with home directory, bash shell, sudo group, password and expiry date

useradd -m -s /bin/bash -G sudo -p $(openssl passwd -1 <password>) -e <date> -c "<comment>" <username> -> it is used to add the user with home directory, bash shell, sudo group, password, expiry date and comment


cat /etc/passwd -> it is used to show the list of users






sudo password -> it is used to change the password of the user

sudo passwd <username> -> it is used to change the password of the user

sudo passwd -l <username> -> it is used to lock the user

sudo passwd -u <username> -> it is used to unlock the user

sudo passwd -d <username> -> it is used to delete the password of the user

sudo passwd -S <username> -> it is used to show the status of the user
show : Dip P 2026-01-26 0 99999 7 -1

Dip P 2026-01-26 0 99999 7 -1
│   │     │       │    │   │
│   │     │       │    │   └─ Account expiration (-1 = never expires)
│   │     │       │    └──── Warning days before password expiry
│   │     │       └──────── Maximum password age (days)
│   │     └──────────────── Minimum password age (days)
│   └────────────────────── Password status
└────────────────────────── Username

field-by-field explanation

Dip
Username

P
Password status

P = password is set

L = account locked

NP = no password

2026-01-26
Last password change date

0
Minimum days between password changes
→ User can change password immediately

99999
Maximum password age
→ Password effectively never expires

7
Warning period (days)
→ User is warned 7 days before password expiration

-1
Account expiration
→ Account never expires

sudo chage -l <username> -> it is used to show the status of the user

sudo passwd -x <days> <username> -> it is used to set the expiry date of the user

sudo passwd -n <days> <username> -> it is used to set the minimum days of the user

sudo passwd -w <days> <username> -> it is used to set the warning days of the user

sudo passwd -i <days> <username> -> it is used to set the inactive days of the user

sudo passwd -e <username> -> it is used to set the expiry date of the user

sudo passwd -l <username> -> it is used to lock the user

sudo passwd -u <username> -> it is used to unlock the user

whoami -> it is used to show the current user

su <username> -> it is used to switch the user

sudo su <username> -> it is used to switch the user with sudo

sudo su - <username> -> it is used to switch the user with sudo and home directory

sudo su - -> it is used to switch the user with sudo and home directory

sudo su -> it is used to switch the user with sudo



sudo userdel <username> -> it is used to delete the user

if the user has home directory then it will not be deleted
and it show proccess id 

sudo userdel -r <username> -> it is used to delete the user and home directory

sudo rm -rf /home/Dip -> it is used to delete the home directory of the user




just userdel are not enough to delete the user completely
we need to delete the user from

Step 1: Confirm where Dip still exists

getent passwd Dip
getent shadow Dip
getent group Dip

Step 2: Check the user ID (optional but useful)
id Dip

Step 3: Remove the user cleanly (force if necessary)

sudo pkill -u Dip 2>/dev/null
sudo userdel -r -f Dip
sudo rm -rf /home/Dip -> it is used to delete the home directory of the user

Step 4: Remove leftover group (very common cause)
sudo groupdel Dip 2>/dev/null


Step 5: Verify complete removal

getent passwd Dip
getent group Dip




groupadd -> it is used to add the group

groupadd <groupname> -> it is used to add the group


cat /etc/group -> it is used to show the group list


in below ,this are not neccessary

groupadd -g <gid> <groupname> -> it is used to add the group with gid

groupadd -g <gid> -r <groupname> -> it is used to add the group with gid and system group

groupadd -g <gid> -r -f <groupname> -> it is used to add the group with gid, system group and force

groupadd -g <gid> -r -f -p <password> <groupname> -> it is used to add the group with gid, system group, force and password

groupadd -g <gid> -r -f -p <password> -e <date> <groupname> -> it is used to add the group with gid, system group, force, password and expiry date

groupadd -g <gid> -r -f -p <password> -e <date> -c "<comment>" <groupname> -> it is used to add the group with gid, system group, force, password, expiry date and comment

groupadd -g <gid> -r -f -p <password> -e <date> -c "<comment>" -s <shell> <groupname> -> it is used to add the group with gid, system group, force, password, expiry date, comment and shell







sudo gpasswd -a <username> <groupname> -> it is used to add the user to the group


sudo gpasswd -d <username> <groupname> -> it is used to remove the user from the group

sudo gpasswd -A <username1>,<username2> <groupname> -> it is used to add the user to the group as admin

sudo gpasswd -M <username1>,<username2> <groupname> -> it is used to add the user to the group as member

sudo gpasswd -r <groupname> -> it is used to remove the password from the group
sudo gpasswd -R <groupname> -> it is used to remove the group from the system



sudo groupdel <groupname> -> it is used to delete the group

sudo groupdel -f <groupname> -> it is used to delete the group forcefully


folder / file -> permission


drwxrwxrwx 
d -> directory
r -> read
w -> write
x -> execute
d{rwx}{rwx}{rwx}
d{user/owner}{group}{other}
rwx -> owner
rwx -> group
rwx -> other


0 0 0 -> 0 <- - - -
0 0 1 -> 1 <- - - x
0 1 0 -> 2 <- - w -
0 1 1 -> 3 <- - w x
1 0 0 -> 4 <- r - -
1 0 1 -> 5 <- r - x
1 1 0 -> 6 <- r w -
1 1 1 -> 7 <- r w x

example:
with director call folder
drwxrwxrwx -> 777
drwxr-x
r-x -> 755
drwxr-x--- -> 750
drwx------ -> 700
drw-rw-rw- -> 666
drw-rw---- -> 660
drw-r----- -> 640
drw------- -> 600
d--x--x--x -> 111
d--------- -> 000

without directory call file
-rwxrwxrwx -> 777
-rwxr-xr-x -> 755
-rwxr-x--- -> 750
-rwx------ -> 700
-rw-rw-rw- -> 666
-rw-rw---- -> 660
-rw-r----- -> 640
-rw------- -> 600
---x--x--x -> 111
---------- -> 000


change folder/file permission

sudo chmod 755 <folder/file> -> it is used to change the permission of the folder/file

sudo chmod -R 755 <folder/file> -> it is used to change the permission of the folder/file recursively

symbolic permission

sudo chmod u=rwx,g=rx,o=rx <folder/file> -> it is used to change the permission of the folder/file

sudo chmod -R u=rwx,g=rx,o=rx <folder/file> -> it is used to change the permission of the folder/file recursively


umask -> it is used to set the default permission of the folder/file

umask 022 -> it is used to set the default permission of the folder/file


sudo chown <username> <folder/file> -> it is used to change the owner of the folder/file

sudo chown <username>:<groupname> <folder/file> -> it is used to change the owner and group of the folder/file


sudo chgrp <groupname> <folder/file> -> it is used to change the group of the folder/file



compress file


zip file.zip file1 file2 file3 -> compress the file

zip -r file.zip folder -> compress the folder recursively


unzip -> unzip file.zip


tar -> tar -cvf file.tar file1 file2 file3

untar -> tar -xvf file.tar

tar with gzip -> tar -czvf file.tar.gz file1 file2 file3

untar with gzip -> tar -xzvf file.tar.gz


c → Create a new archive

z → Compress with gzip

v → Show all files while adding

f Dip_backup.tar.gz → Save the archive as Dip_backup.tar.gz




x → Extract the archive

z → Decompress with gzip

v → Show all files while extracting

f Dip_backup.tar.gz → Extract the archive Dip_backup.tar.gz