## ad hoc 

Ad hoc command is a way to run a single, simple task on one or more nodes without writing a full playbook. 
Ad hoc commands are useful for quick, one-off tasks or for troubleshooting and testing. 
They are executed directly from the command line using the ansible command.

## Example command:

```aansible all -i /etc/ansible/inventory -m ping```

ansible all= the ad hoc command to to traget on group 'all', so basically in this case it will target all host mentioned in the inventory file.

-i= 'i' flag means inventory file and followed by the inventory file path. It coould be of any name such as inventory, hosts, etc 

-m= 'm' flag means module, in this case its ping module.


-----------------------------------------------------------------------------
 ## Example command:

```ansible webserver -i /etc/ansible/inventory -m ping```

so it will just ping one group, i.e webserver


