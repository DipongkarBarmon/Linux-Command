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



 