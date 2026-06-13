
Part A: Understanding Users

Answers
What is your current username?
The current username is the logged-in user shown by:
Bash
whoami
Example output:
Bash
kali

What is UID?
UID stands for User ID.
It is a unique number assigned to every user in Linux.
Example:
Bash
uid=1000(kali)

What is GID?
GID stands for Group ID.
It identifies the primary group of the user.
Example:
Bash
gid=1000(kali)

What information does /etc/passwd contain?
The /etc/passwd file contains:
Username
User ID (UID)
Group ID (GID)
Home directory
Default shell
Example entry:
Bash
kali:x:1000:1000:Kali User:/home/kali:/bin/bash


Part B: Create Users & Groups
Create Groups

sudo groupadd interns
sudo groupadd cyberteam
Create Users

sudo useradd -m student1
sudo useradd -m student2
sudo useradd -m student3
Set Passwords

sudo passwd student1
sudo passwd student2
sudo passwd student3
Add Users to Groups

sudo usermod -aG interns student1
sudo usermod -aG cyberteam student2
sudo usermod -aG interns,cyberteam student3
Verify Users & Groups
Check groups
groups
Check user details
Bash
id student1
id student2
Example Output
Bash
uid=1001(student1) gid=1001(student1) groups=1001(student1),1002(interns)

uid=1002(student2) gid=1002(student2) groups=1002(student2),1003(cyberteam)
Part C: File Ownership
Commands
Bash
mkdir CyberSecurity_Project
cd CyberSecurity_Project

touch report.txt notes.txt credentials.txt
Check Ownership
Bash
ls -l
Change Ownership of File
Bash
sudo chown user2 report.txt
Example Output
Bash
-rw-r--r-- 1 user1 user1 0 Jun 13 10:00 report.txt
After changing owner:
Bash
-rw-r--r-- 1 user2 user1 0 Jun 13 10:00 report.txt
Documentation
Original Owner: user1
New Owner: user2
Command Used:
Bash
sudo chown user2 report.txt


Part D: File Permissions
Create File
touch security_policy.txt
Check Permissions

ls -l
Modify Permissions
Read Only

chmod 444 security_policy.txt
Permission:

-r--r--r--
Read + Write
Bash
chmod 666 security_policy.txt
Permission:

-rw-rw-rw-
Read + Write + Execute
Bash
chmod 777 security_policy.txt
Permission:

-rwxrwxrwx
Example Output
Bash
-rw-r--r-- 1 kali kali 0 Jun 13 10:10 security_policy.txt


Part E: Permission Analysis
Permission
Owner Rights
Group Rights
Other User Rights
Real-world Use Case
755
Read, Write, Execute
Read, Execute
Read, Execute
Used for program files and directories where everyone can access but only owner can modify
644
Read, Write
Read
Read
Common for text files and documents
777
Read, Write, Execute
Read, Write, Execute
Read, Write, Execute
Temporary shared files; not secure for sensitive data
600
Read, Write
No Access
No Access
Private files like passwords or SSH keys
700
Read, Write, Execute

Personal scripts or private directories


Part F: Security Challenge
File
Recommended Permission
Reason
password_backup.txt

600
Contains sensitive passwords, only owner should access
public_notice.txt

644
Everyone can read the notice but only owner can edit
system_log.txt

640
Owner can read/write, group can read for monitoring
personal_notes.txt

600
Personal information should stay private
Explanation
Sensitive files should have limited access.
Public files can allow read access to others.
System logs may need group access for administrators.
Private notes and passwords must not be accessible to other users.


Part G: Linux Security Research

1. Why are file permissions important?
File permissions protect files from unauthorized access, modification, or deletion. They help maintain system security and privacy.

2. What happens if sensitive files are given 777 permissions?
Any user can read, modify, or delete the file. This creates major security risks such as data theft or system damage.

3. What is the principle of Least Privilege?
Users should get only the minimum permissions needed to perform their tasks. This reduces security risks.

4. Why do organizations restrict user access?
Organizations restrict access to protect confidential data, prevent misuse, reduce cyber attacks, and maintain system stability.