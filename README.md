Part A: Linux Installation & Verification
Installed Operating System
Kali Linux on Virtual Machine (VM)


Part B: Basic Navigation Commands
1. pwd
Purpose
pwd command is used to display the current working directory.
Command
Bash
pwd
Example Output
Bash
/home/kali

3. ls
Purpose
ls command is used to list files and folders in the current directory.
Command
Bash
ls
Example Output
Bash
Desktop  Documents  Downloads  Pictures

5. ls -la
Purpose
ls -la command shows all files including hidden files with detailed information.
Command
Bash
ls -la
Example Output
Bash
drwxr-xr-x  Desktop
drwxr-xr-x  Downloads
-rw-r--r--  file.txt

7. cd
Purpose
cd command is used to change the directory.
Command
Bash
cd Documents
Example Output
Bash
Changed to Documents directory

9. clear
Purpose
clear command is used to clear the terminal screen.
Command
Bash
clear
Example Output
Bash
Terminal screen cleared

11. history
Purpose
history command displays previously used commands.
Command
Bash
history
Example Output
Bash
1 pwd
2 ls
3 cd Documents
4 clear

13. whoami
Purpose
whoami command shows the current logged-in username.
Command
Bash
whoami
Example Output
Bash

kal
14. hostname
Purpose
hostname command displays the system hostname.
Command
Bash
hostname
Example Output
Bash
kali-linux


Part C: Directory Management
Commands
Bash
mkdir CyberSecurity_Lab
cd CyberSecurity_Lab

mkdir Networking
mkdir Linux
mkdir CyberSecurity
mkdir EthicalHacking
mkdir Reports

tree
Output
Bash
CyberSecurity_Lab
├── Networking
├── Linux
├── CyberSecurity
├── EthicalHacking
└── Reports


Part D: File Management
Create Files
Bash
touch notes.txt
touch commands.txt
touch report.txt
Copy Files
Bash
cp notes.txt notes_copy.txt
Move Files
Bash
mv report.txt Reports/
Rename Files
Bash
mv commands.txt linux_commands.txt
Delete Files
Bash
rm notes_copy.txt
What Each Command Does
Command
Purpose
mkdir
Creates a new directory/folder
cd
Changes current directory
tree
Shows folder structure
touch
Creates empty files
cp
Copies files
mv
Moves or renames files
rm
Deletes files
Part E: System Information Collection
Commands:
Bash
uname -a
hostname
whoami
date
uptime
pwd
Example Output:
Bash
$ uname -a
Linux kali 6.1.0-kali7-amd64 #1 SMP Debian x86_64 GNU/Linux

$ hostname
hp-pekdosk

$ whoami
kali

$ date
Wed Jun 11 08:45:10 PM IST 2026

$ uptime
20:45:10 up 2 hours, 15 minutes, 1 user, load average: 0.10, 0.15, 0.20

$ pwd
/home/kali
R
Part F: Linux Research Activity
1. What is Linux?
Linux is an open-source operating system used to manage computer hardware and software. It is widely used in servers, cybersecurity, programming, and networking.
2. Why is Linux important in Cyber Security?
Linux is important in cybersecurity because it is secure, stable, and supports many security tools. Ethical hackers and security professionals use Linux for penetration testing, monitoring, and network analysis.

4. Difference between Linux and Windows
Linux
Windows
Open-source operating system
Proprietary operating system
More secure and customizable
Easy to use for beginners
Mostly used in servers and cybersecurity
Mostly used for personal and office work
Free to use
Requires license

6. What is a Linux Distribution?
A Linux distribution is a version of Linux that includes the Linux kernel, software packages, and user interface. Examples are Ubuntu, Kali Linux, Fedora, and Debian.
7. Why do Ethical Hackers prefer Linux-based operating systems?
Ethical hackers prefer Linux because it provides powerful command-line tools, better security, flexibility, and support for cybersecurity tools like Nmap, Wireshark, and Metasploit.
