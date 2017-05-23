Network
===
Which ports are wired:
		netstat --listen
		lsof -i
		
Useful filters:
		// all open IPV4 connections from PID
		lsof -i 4 -a -p 1
		
Test if you can connect to a port on a machine:
	remote box: nc -l 5000
	local box: nc -z -v REMOTE_BOX_NAME 5000