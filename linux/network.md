#Network
Which ports are wired:
		netstat --listen
		netstat -l
		lsof -i :PORT_NUMBER
		
Useful filters:
		// all open IPV4 connections from PID
		lsof -i 4 -a -p 1
		
Or with netcat (because the name is soo cool):
	remote box: nc -l 5000
	local box: nc -z -v REMOTE_BOX_NAME 5000
	
	// Which machines are online in the same network
	nmap -sP X.X.X.0/24
	
	// which machinses are web servers (listening on typical ports)
	nmap -sT -p 80,8080,443,8443 X.X.X.0/24
	// same but ninja stealth mode
	nmap -sS -p 80,8080,443,8443 X.X.X.0/24
	// same but with white ninja decoy
	nmap -sS -p 80,8080,443,8443 -D 1.1.1.1 X.X.X.0/24
	
	// guess OS
	sudo nmap -O 192.168.1.1
	
	// detect versions of software running on opened ports etc. COOL STUFF
	sudo nmap -A 192.168.1.1
	