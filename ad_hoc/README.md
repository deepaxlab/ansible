ad hoc 

Ad hoc command is a way to run a single, simple task on one or more nodes without writing a full playbook. 
Ad hoc commands are useful for quick, one-off tasks or for troubleshooting and testing. 
They are executed directly from the command line using the ansible command.

Example command:

ansible all -i /etc/ansible/inventory -m ping 

#used to ping the nodes in the inventory

