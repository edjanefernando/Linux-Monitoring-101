# Linux-Monitoring-101
* Monitoring 101 Module: 
* Linux Administration Competence: is able to gather information about the state of a linux machine Type of Challenge: Consolidation Duration: 
* 3 day Deadline: 09/04/2024 
* Participants: : solo

# The Mission
One of the most important responsibilities a system administrator or SOC analyst have is monitoring the systems he manages. Indeed it's one thing to set them up and install software on them, but then what!? Well the next step is ensuring that the machines you provisioned as well as the services you deployed on them remain available, reliable and secure! This challenge is divided in two tasks, the first one having you research how to monitor a Linux system as well as what to look for when doing so. You will have to take note of all your findings in a text file (EX: markdown) while being as exhaustive as possible (what to monitor, how to monitor it, commands used, ...). Try to answer, but don't limit yourself to, the questions below to guide you through the research process:

* What are the main area of concern when monitoring a system? (EX: CPU load, disk usage, ...)
* How can you check what are the most memory intensive running processes ?
* What are log files? Where can you fin them on a typical Linux system ?
* How can you check who where the last connected users, what they did, when they left ?
* What are the different metrics of health and performance of a system ?
* How can you check the uptime of a machine ?
* How can you assess the network traffic ?
* The second task is meant to serve as practice and will have you, in a different file, write a report with as many relevant information (what would make sense in a report) as you can muster on a system you manage. It most preferably would be a remote machine, but it can also be your local machine as this is just practice.

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


