# Day 11: Networking Basics – Check and Monitor Network Information with ip, ping, netstat, ss, and hostname

## 🗓️ Date  
2025-08-10

## ✅ Goal  
Learn how to view network configuration, test connectivity, monitor network connections, and check system hostname using basic Linux networking commands.

## 🗂️ Key Commands and Their Purpose  
Command / Syntax                        | Description  
----------------------------------------|---------------------------------------------  
ip addr                                 | Display network interfaces and IP addresses  
ip link                                 | Show network interfaces and their status  
ping <hostname/IP>                      | Test connectivity to another host or IP address  
netstat -tuln                           | Show active listening ports and associated services  
ss -tuln                                | Faster, modern replacement for netstat to view network connections  
hostname                                | Display the current system hostname  
hostnamectl                             | View or set system hostname and related settings  

## 🔍 What I Did Today  
- Checked all IP addresses and network interfaces:
  ```bash
  ip addr

## 🧠 Notes
- ip addr is the modern alternative to the older ifconfig.
- Use ping -c <count> to limit the number of pings instead of running indefinitely.
- netstat is often deprecated; ss is preferred for speed and modern protocol support.
- Hostname is important for identifying your machine in a network.
- Changing the hostname may require sudo and can affect network recognition.