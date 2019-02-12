Commands used in ssh workshop::

	1)To intsall ssh use command 
		-sudo apt-get update
		-sudo apt-get install openssh-server
		-sudo apt-get install openssh-client
		
	2)To connect to remote system with ssh protocol
		-ssh user_name@ ip_address -p port_no.:
				-used to connect to a remote system with user name as user_name , ip address as ip_address
				 and port number as port_no

	3)To open an editor
		gedit file_name
			-opens a graphical editor
			-opens a new file if doesn't exist
		vim fil_name 
			-open vim editor 
			-opens new file if it does not exist 
			- press e to enter to edit mode and ESC key to exit it
			- press colon(:) to enter any command in vim editor
			- wq is for save and exit vim
		nano file_name 
			-opens a nano editor with a name file_name
			-opens a new file if file doesn't exist
			- press CTRL+O to save
			- press CTRL+X to exit
	4)Command used to display the chat
		tail:
			-displays last content of a file
			- '-f' option will displays last written lines of a file and  continusely  updates it
	5)Command used to change the directory	
		cd:change directory
	6)command used for displaying files
		ls:list
	7)TYPE man and the command name to open the  mannual of any command or type command --help
		e.g man ls 
			or
		    ls --help
		
Secure Shell
-Secure Shell is a cryptographic network protocol for operating network services securely over an unsecured network.
-The best known example application is for remote login to computer systems by users.	

Updating Security
-To secure ssh go to etc directory and then to ssh directory and open any editor to update sshd_config file and change the following settings-
	-change port number to any port no other than 22
	-copy the public key of your device to the remote device 
	-remove password authentication
Chating With ssh
-To chat using ssh create a file in remote server
-open that file in an editor in one terminal and open another terminal and type tail -f file_name
-now see the magic

Proxy 
- Change the port number of the remote system to 443
- open terminal in your device and type this command;
			ssh -N -D 4444 uname@ip 
- open your system's browser 
- go to preferences -> then network settings -> advance -> click on mannual proxy and in SOCKS Host type 127.0.0.1 in ip and 4444 in port
