# 4.Execution_of_NetworkCommands
Name: R.Sabarinath
Register No:212223100048
## AIM 
Use of Network commands in Real Time environment
## SOFTWARE
Command Prompt And Network Protocol Analyzer
## PROCEDURE 
To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>
## PROGRAM
## PING COMMAND
## CLIENT
```
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost'8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
```
## SERVER
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```
## TRANCEROUTE COMMAND
```
from scapy.all import* 
target = ["www.google.com"] 
result, unans = traceroute(target,maxttl=32) 
print(result,unans)
```
## OUTPUT
## PING COMMAND CLIENT
## CLIENT
![image](https://github.com/Sabari-2005/4.Execution_of_NetworkCommends/assets/139338709/6b916989-e2c3-44aa-8aa3-36bfe2513750)
## SERVER
![image](https://github.com/Sabari-2005/4.Execution_of_NetworkCommends/assets/139338709/42535798-083c-41b5-bcd5-a85d0a2dfa86)
## TRANCEROUTE COMMAND
![image](https://github.com/Sabari-2005/4.Execution_of_NetworkCommends/assets/139338709/eb8565b0-1d66-4274-aece-c589f371e689)

## RESULT
Thus Execution of Network commands Performed 
