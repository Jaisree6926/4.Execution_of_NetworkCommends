# 4.Execution_of_NetworkCommands
## name:Jaisree B
## reg no:212224230100
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
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

## program
## client
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

## server
    import socket 
    s=socket.socket() 
    s.connect(('localhost',8000)) 
    while True: 
        ip=input("Enter the website you want to ping ") 
        s.send(ip.encode()) 
        print(s.recv(1024).decode())
## Output
## client
![322405336-b53ac2f5-24c7-481c-bc98-cf5db18d2510](https://github.com/user-attachments/assets/03516fe8-5697-43d6-b957-79a7d42ae8f4)
## server
![322405458-c09a7fe7-d19b-425f-bcd0-db6570c949a2](https://github.com/user-attachments/assets/4012e188-dfbd-40c1-8dec-75c726c4a138)

## TRANCEROUTE COMMAND
    from scapy.all import* 
    target = ["www.google.com"] 
    result, unans = traceroute(target,maxttl=32) 
    print(result,unans)


![322405553-2c9ce9c5-56bf-496f-b39c-86176db284ae](https://github.com/user-attachments/assets/64ad2150-cfb0-408d-b02f-61ac7ed34918)


## Result
Thus Execution of Network commands Performed 
