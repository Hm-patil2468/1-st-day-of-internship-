Part A: Process Monitoring
1. What is a Process?
A Process is a running instance of a program in Linux.
Example: browser, terminal, music player, etc.

2. What is a PID?
PID (Process ID) is a unique number given to every running process by the operating system.

3. Which process is consuming the most CPU?
Use the command:
Bash
top
or
Bash
htop
The process shown at the top with the highest %CPU value is consuming the most CPU.
Example answer:
Plain text
Process: firefox
CPU Usage: 45%

4. Which process is consuming the most Memory?
Use:
Bash
top
or
Bash
htop
The process with the highest %MEM value is consuming the most memory.
Example answer:
Plain text
Process: chrome
Memory Usage: 18%

Part B: Process Management

Step 1: Start a Process
Bash
sleep 300

Step 2: Find the Process

ps aux | grep sleep
Example Output:

user   2456  0.0  0.1  sleep 300
Here:
Process Name = sleep
PID = 2456

Step 3: Terminate the Process
Bash
kill 2456
If it does not stop, use:
Bash
kill -9 2456
Documentation
PID Found:
Plain text
2456
Command Used:
Bash
ps aux | grep sleep
kill 2456
Result:
Plain text
The sleep process was terminated successfully.


Part C: System Monitoring
Commands Used
Bash
free -h
df -h
uptime
uname -a
System Summary Report
Total RAM: 4 GB
Available RAM: 2.5 GB
Disk Usage: 20 GB used out of 50 GB
System Uptime: 3 hours 25 minutes
Kernel Version: Linux 5.15.0-84-generic x86_64
Explanation
free -h → Shows memory usage (RAM).
df -h → Displays disk space usage.
uptime → Shows how long the system has been running.
uname -a → Displays kernel and system information.

Part D: Service Monitoring
Commands Used

1. What is a Service?
A service is a background program that runs continuously to perform system tasks such as networking, SSH access, printing, or web hosting.

2. Why are services important?
Services are important because they help the operating system perform essential functions automatically and keep the system running smoothly.

3. How can a stopped service affect a system?
If a service stops, related functions may stop working.
Example:
If the SSH service stops, remote login will not work.
If NetworkManager stops, internet/network connection may fail.
Example Service Status
SSH Service: Active and running
NetworkManager Service: Active and running


Part E: Shell Scripting
Script Name:
system_report.sh
Script Code:
Bash
#!/bin/bash

echo "System Information Report"
echo "--------------------------"

echo "User: diuu
echo "Hostname: hm-peskdosk
echo "Date: 12-5-2026
echo "Current Directory: text

echo ""
echo "Memory Usage:"
free -h

echo ""
echo "Disk Usage:"
df -h
Steps to Execute:
Bash
nano system_report.sh


Bash
chmod +x system_report.sh
Run the script:
Bash
./system_report.sh
Example Output:
Bash
System Information Report
--------------------------

Part F: Security Monitoring Challenge
1. netstat
Purpose:
Displays network connections, routing tables, and listening ports.
Example Command:
Bash
netstat -tulnp
Example Output:
Bash
tcp   0   0 0.0.0.0:22   0.0.0.0:*   LISTEN
Security Use Case:
Used to detect suspicious open ports and active network connections.

2. ss
Purpose:
Shows socket statistics and network connections.
Example Command:
Bash
ss -tuln
Example Output:
Bash
tcp LISTEN 0 128 0.0.0.0:80
Security Use Case:
Helps monitor active services and identify unusual connections.

3. who
Purpose:
Displays users currently logged into the system.
Example Command:
Bash
who
Example Output:
Bash
student  pts/0  2026-06-13 10:00
Security Use Case:
Used to check unauthorized user logins.

4. w
Purpose:
Shows logged-in users and their current activities.
Example Command:
Bash
w
Example Output:
Bash
USER   TTY   FROM        LOGIN@   IDLE
student pts/0 192.168.1.5 10:00   2:00
Security Use Case:
Helps administrators monitor user activity and system usage.

5. last
Purpose:
Displays login history of users.
Example Command:
Bash
last
Example Output:
Bash
student pts/0 192.168.1.5 Fri Jun 13