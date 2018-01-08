Network
===
Which ports are wired:
		netstat --listen
		netstat -l
		lsof -i
		
Useful filters:
		// all open IPV4 connections from PID
		lsof -i 4 -a -p 1
		
Or with netcat (because the name is soo cool):
	remote box: nc -l 5000
	local box: nc -z -v REMOTE_BOX_NAME 5000
	
	
### Which machines are online in the same network
	nmap -sP X.X.X.0/24