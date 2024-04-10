# Linux-Monitoring-101
* Monitoring 101 Module: 
* Linux Administration Competence: is able to gather information about the state of a linux machine Type of Challenge: Consolidation Duration: 
* 3 day Deadline: 09/04/2024 
* Participants: : solo

# The Mission
One of the most important responsibilities a system administrator or SOC analyst have is monitoring the systems he manages. Indeed it's one thing to set them up and install software on them, but then what!? Well the next step is ensuring that the machines you provisioned as well as the services you deployed on them remain available, reliable and secure! This challenge is divided in two tasks, the first one having you research how to monitor a Linux system as well as what to look for when doing so. You will have to take note of all your findings in a text file (EX: markdown) while being as exhaustive as possible (what to monitor, how to monitor it, commands used, ...). Try to answer, but don't limit yourself to, the questions below to guide you through the research process:

1.  What are the main area of concern when monitoring a system? (EX: CPU load, disk usage, ...)

- CPU Load: Monitor CPU utilization to ensure optimal performance and detect any spikes or abnormalities.
1. CPU Load:
Command: top
Description: top provides real-time information about CPU usage, including a list of processes sorted by their CPU consumption.
Usage: Run the top command in your terminal. Look at the %CPU column to see the CPU usage of each process.
![image](https://github.com/edjanefernando/Linux-Monitoring-101/assets/141014730/fe90fad3-d104-4295-9652-79bb0412d9b3)

- Memory Usage: Track memory usage to prevent system slowdowns or crashes caused by memory exhaustion.
Memory Usage:
Command: free -m
Description: free -m displays the amount of free and used memory in the system.

Usage: Execute the free -m command in your terminal. It will show you the total amount of memory, used memory, free memory, and memory used for caching purposes.
![image](https://github.com/edjanefernando/Linux-Monitoring-101/assets/141014730/3ac88988-4cdd-4dbb-ac5c-5f701f5fb014)

- Disk Usage: Monitor disk space to prevent storage-related issues and ensure sufficient space for system operation.
 Disk Usage:
Command: df -h
Description: df -h displays the amount of disk space used and available on mounted file systems.
Usage: Run the df -h command in your terminal. It will show you a list of mounted file systems along with their disk usage information.

![image](https://github.com/edjanefernando/Linux-Monitoring-101/assets/141014730/0394deee-5015-4bf2-8800-1cac22ff6f84)

- Network Activity: Monitor network traffic to detect anomalies, potential attacks, or network congestion.
Network Activity:
Command: iftop or nload
Description: iftop and nload provide real-time monitoring of network interfaces, displaying incoming and outgoing traffic rates.
Usage: Install iftop or nload if they are not already installed on your system. Then run iftop or nload in your terminal to monitor network activity.
If you're encountering the "command not found" error when trying to run sudo iftop or sudo nload, it likely means that the iftop or nload package is not installed on your system. Here's how you can fix it:

Option 1: Install iftop or nload using package manager:
For iftop:
Run the following command to install iftop using the package manager:  **sudo apt-get install iftop**

![image](https://github.com/edjanefernando/Linux-Monitoring-101/assets/141014730/2172db28-d061-4728-99f3-96fc27963f6f)


For nload:
Run the following command to install nload using the package manager: **sudo apt-get install nload**

![image](https://github.com/edjanefernando/Linux-Monitoring-101/assets/141014730/edf72043-40fc-423e-8da9-1d7b24c991d1)



- Processes: Keep track of running processes to identify resource-intensive applications or unauthorized activities.
- Security Events: Monitor system logs for security-related events, such as failed login attempts or privilege escalation attempts.

2. How can you check what are the most memory intensive running processes ?

To check the most memory-intensive running processes on a Linux system, you can use the top command or its more interactive counterpart htop

* Using  command : **top**

![image](https://github.com/edjanefernando/Linux-Monitoring-101/assets/141014730/10a8c75d-7c01-44da-b1d8-46b6f43a6bd0)

top will display a list of processes sorted by CPU usage. To sort by memory usage, press Shift + M.

![image](https://github.com/edjanefernando/Linux-Monitoring-101/assets/141014730/70417d61-ce2e-411d-bef4-a2f69beff21d)

You will now see the processes sorted by their memory usage, with the most memory-intensive processes listed at the top.


* Using  command : **htop**

If htop is not installed, you can install it using your package manager. For example, on Ubuntu, you can install it with:

**sudo apt-get install htop**

![image](https://github.com/edjanefernando/Linux-Monitoring-101/assets/141014730/c1391657-c0e7-454a-8772-ea59667b4c6d)

Command htop will display an interactive list of processes, with memory usage information prominently displayed.

By default, processes are sorted by CPU usage. To sort by memory usage, press F6 to enter the "SortBy" menu, then select MEM% and press Enter.
![image](https://github.com/edjanefernando/Linux-Monitoring-101/assets/141014730/efe245e6-6d92-45e9-9ffb-223eb6ba26e8)

You will now see the processes sorted by their memory usage, with the most memory-intensive processes listed at the top

3. What are log files? Where can you fin them on a typical Linux system ?


Log files are records of events and actions that occur on a system. They provide valuable information for troubleshooting, auditing, and monitoring system activities. Log files contain various types of information, including system messages, error reports, user actions, authentication attempts, and more.

- On a typical Linux system, log files are stored in the /var/log/ directory. Here are some common log files you may find in this directory:

* syslog: The main system log file that contains messages from various system services and applications.

* auth.log: Logs authentication-related events, such as successful and failed login attempts.

* kern.log: Logs kernel-related messages and errors.

* messages: General system messages and errors.

* dpkg.log: Logs package installation, removal, and upgrade activities.

* apache2/access.log and apache2/error.log: Logs Apache web server access and error events, respectively.

* mysql/error.log: Logs MySQL database server errors and warnings.

* nginx/access.log and nginx/error.log: Logs Nginx web server access and error events, respectively.

View Log Files: You can view the contents of specific log files using a text editor like nano or less, or you can use commands like cat or tail to display the contents directly in the terminal.

For example, to view the contents of the syslog file, you can use the less command:

![image](https://github.com/edjanefernando/Linux-Monitoring-101/assets/141014730/c03d3c3c-ad5c-4f5d-9782-2f4a5a3821fb)


4. How can you check who where the last connected users, what they did, when they left ?


5. What are the different metrics of health and performance of a system ?


7. How can you check the uptime of a machine ?
8. How can you assess the network traffic ?
9. The second task is meant to serve as practice and will have you, in a different file, write a report with as many relevant information (what would make sense in a report) as you can muster on a system you manage. It most preferably would be a remote machine, but it can also be your local machine as this is just practice.

IMPORTANT: Take your time when researching, it's the most important part of this challenge as you'll need to be able to find out what is happening on any given system at any given time. Whether it's the percentage of system's resources currently used, what commands are being run, who is logged in, and so on...

Complementary Resources
Useful monitoring commands
Linux system monitoring fundamentals
Final Words
There are plenty of tools out there but remember that collecting the metrics is only the first step towards an end goal, which is, to be able to keep track of the state of machines, troubleshoot them to understand errors and in the best cases prevent issues before they even happen!

One last thing, we cannot understate how important, even crucial, monitoring for servers, services and applications deployment.

## Introduction
Monitoring a Linux system is crucial for maintaining its availability, reliability, and security. 
System administrators and SOC analysts need to continuously gather information about the state of the systems they manage.
This document outlines key areas of concern, methods for monitoring, and relevant commands to achieve effective system monitoring.

## Main Areas of Concern
* CPU Load: Monitor CPU utilization to ensure optimal performance and detect any spikes or abnormalities.
* Memory Usage: Track memory usage to prevent system slowdowns or crashes caused by memory exhaustion.
* Disk Usage: Monitor disk space to prevent storage-related issues and ensure sufficient space for system operation.
* Network Activity: Monitor network traffic to detect anomalies, potential attacks, or network congestion.
* Processes: Keep track of running processes to identify resource-intensive applications or unauthorized activities.
* Security Events: Monitor system logs for security-related events, such as failed login attempts or privilege escalation attempts.
* Memory Intensive Processes
* To identify the most memory-intensive processes, use the top command or htop for a more interactive view. These commands provide real-time information about CPU and memory usage, along with a list of running processes sorted by resource consumption.

## Log Files
Log files are records of events and actions that occur on a system. They provide valuable information for troubleshooting and auditing purposes. Log files are typically located in the /var/log directory on a Linux system. Common log files include syslog, auth.log, messages, and kernel.log.

Last Connected Users and Activity
To check the last connected users and their activity, use the last command. It displays a list of recent login sessions, including the login time, duration, and source IP address. Additionally, the w command provides information about currently logged-in users and their activities.

## System Health and Performance Metrics
Key metrics for assessing system health and performance include:

CPU Utilization: Percentage of CPU resources in use.
Memory Usage: Amount of RAM utilized by processes.
Disk Space: Available disk space and utilization.
Network Throughput: Incoming and outgoing network traffic.
Load Average: Average number of processes waiting for CPU time over a period.
Uptime of a Machine
To check the uptime of a machine, use the uptime command. It provides information about how long the system has been running, the current time, number of users, and system load averages.

## Network Traffic Assessment
To assess network traffic, use tools like iftop or nload. These tools provide real-time monitoring of network interfaces, displaying incoming and outgoing traffic rates, as well as the total amount of data transferred.

## Conclusion


