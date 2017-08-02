###General
 - Runs everything via ssh. 
 - Nodes must have python installed
 - Is an orchestration framework

Inventory lists
	- basically list of hosts
	- may be generated
	- support variables
	
Playbooks 
 - basically list of commands
 - describe the desired end-state
 - have variables (multiple ways to set them)
 - contain plays
 
Modules
 - automate nearly every part of the given environment
 - run with '-m'
 - dry run with '-C -m'

Plays
 - contain tasks

Tasks
 - contain modules
 - run sequentially
 
Handlers
 - triggered by tasks
 - run once at the end of a play 