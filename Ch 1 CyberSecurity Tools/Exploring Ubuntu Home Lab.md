Firstly I used the "ip a command" to visualize and see all network interfaces and ip addresses connected to this Virtual machine(VM).
![alt text](image.png)

Secondly  the command netstat -tuln will be ran to verfiy which ports are currently open and what state these ports are in.
![alt text](image-1.png)

I should also verify what network connections are currently established to my server using "lsof -i -P -n"
![alt text](image-2.png)

Network Scan sudo nmap -sS -O localhost
![alt text](image-3.png)

 Check for Open Ports on the Server's Network sudo nmap -sP 192.168.1.0/24
 ![alt text](image-4.png)

 Check for Services and Versions sudo nmap -sV localhost

 ![alt text](image-5.png)

 Identify Potential Vulnerabilities sudo nmap --script vuln localhost
 ![alt text](image-6.png)

 Inspect Network Traffic sudo tcpdump -i eth0
![alt text](image-7.png)

 Monitor Network Connections in Real-Time sudo watch -n 1 netstat -tulnp

 ![alt text](image-8.png)

 Check Firewall Rules  sudo ufw status verbose

 ![alt text](image-9.png)
