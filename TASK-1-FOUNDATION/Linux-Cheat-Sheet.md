# Linux Cheat Sheet

## 1. Navigation Commands

Show current directory:
pwd

List files:
ls

List files with details:
ls -l

Show hidden files:
ls -la

Change directory:
cd directory_name

Go to parent directory:
cd ..

## 2. File and Directory Commands

Create a directory:
mkdir folder_name

Create a file:
touch file.txt

Copy a file:
cp file.txt backup.txt

Move or rename a file:
mv old.txt new.txt

Delete a file:
rm file.txt

## 3. File Permissions

View permissions:
ls -l

Change permissions:
chmod 755 file.sh

Change ownership:
chown user:user file.txt

## 4. Package Management

Update package lists:
sudo apt update

Upgrade packages:
sudo apt upgrade

Install a package:
sudo apt install package-name

Remove a package:
sudo apt remove package-name

## 5. Networking Commands

Show IP addresses:
ip addr

Test connectivity:
ping 192.168.100.20

Show routing information:
ip route

Show network connections:
ss -tuln

Trace the network path:
traceroute 192.168.100.20

## 6. File Reading Commands

cat file.txt
less file.txt
head file.txt
tail file.txt

## 7. Searching Commands

Search for text:
grep "text" file.txt

Find a file:
find /path -name "filename"

## 8. System Commands

Display current user:
whoami

Display system information:
uname -a

List running processes:
ps aux

Show command history:
history

Clear terminal:
clear

Open a command manual:
man command

## 9. Cybersecurity Lab Commands

Show network interfaces:
ip addr

Test target connectivity:
ping -c 4 192.168.100.20

Scan target services:
nmap 192.168.100.20

Check SSH port:
nc -zv 192.168.100.20 22

Check OpenSSL version:
openssl version

## 10. Lab Network

Kali Linux:
IP address 192.168.100.10
Interface eth1
Network cyberlab

Metasploitable 2:
IP address 192.168.100.20
Interface eth0
Network cyberlab

## 11. Security Tools

Nmap - Network scanning
Wireshark - Packet capture and analysis
Burp Suite - Web application security testing
Netcat - Network and service testing
OpenSSL - Cryptographic operations

## Important Note

These commands are documented for learning and authorized cybersecurity testing in a controlled laboratory environment.
