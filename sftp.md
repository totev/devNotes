#Config for sftp user in group sftp

sudo nano /etc/ssh/sshd_config

	# override default of no subsystems
	Subsystem       sftp    /usr/lib/openssh/sftp-server

	# Example of overriding settings on a per-user basis
	Match Group sftp
	        ChrootDirectory /ftpusers/HomeFolder/
	        X11Forwarding no
	        AllowTcpForwarding no
	        PermitTTY no
	        ForceCommand internal-sftp