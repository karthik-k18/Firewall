# Firewall
Basic Firewall Configuration and Testing
Objective

The goal of this project is to configure and test basic firewall rules to allow or block specific network traffic using:

Windows Firewall (GUI & CLI via netsh or PowerShell)

UFW (Uncomplicated Firewall) on Linux (Ubuntu/Debian)

This includes allowing/denying ports, IP addresses, and protocols and verifying their effectiveness through testing.

Tools Used
Windows Firewall (Control Panel / PowerShell)

UFW (Uncomplicated Firewall) – preinstalled on many Ubuntu-based distros

Ping / netcat (nc) / telnet / curl for testing

OS: Windows 10 & Ubuntu 22.04

Configuration Steps
On Linux (UFW):

sudo ufw enable

Default Policies
sudo ufw default deny incoming
sudo ufw default allow outgoing

Allow SSH (Port 22)
sudo ufw allow 22

Allow HTTP (Port 80)
sudo ufw allow 80/tcp

Deny a Specific IP
sudo ufw deny from 192.168.1.100

Check Status
sudo ufw status numbered

Sample output
Status: active

To                         Action      From
--                         ------      ----
22                         ALLOW       Anywhere
80/tcp                     ALLOW       Anywhere
Anywhere                   DENY        192.168.1.100
