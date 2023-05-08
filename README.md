# DEVOPS-UBUNTU-20.04-ANSIBLE
DEVOPS-UBUNTU 20.04-ANSIBLE
Assignment No 6
Title: Write a ansible playbook to deploy Apache Web server.
Theory:
1)	What is YAML
[ Please complete this part]

2)	Introduction to Ansible
[ Please complete this part]

Implementation:
1.	Architecture: 




	Figure1: Architecture Diagram
2.	Steps
a)	Create 4 ec2 instances of Ubuntu machine.

 
b)	Connect to “Ansible-Master” server
c)	Write following commands

1)	> sudo -i
2)	> apt update
 
3)	Install ansible using command
	apt install ansible
 

4)	Check the version of ansible using command
	ansible –version
5)	update reaming all hosts i.e. Ansible-Server1, Ansible-Server2, Ansible-Server3 using command


	sudo apt-get update
  
  
  
CLOSE ALL TERMINALS AND DON’T BE ROOT USER IN NORMAL USER RUN ssh-keygen CMD
  
d)	Generate a ssh key on Ansible-master using command
	ssh-keygen
		 
e)	copy the public key which is in .ssh folder into “authorized keys” on ansible-server1
commands: 
	1)  ls ~/.ssh
	2) cat ~/.ssh/id_rsa.pub
 
f)	connect to ansible-server1 and again give command 
		> ssh-keygen
	It will create the same files on ansible-server1
Now,
	> vim ~/.ssh/authorized_keys
		and	Copy the public key 

 


g)	Now login to Ansible-master and try to connect to ansible server using command
	> ssh ubuntu@private-ip

 
	
Create a playbook on Ansible-master 
Step 1:- connect to “Ansible-Master” 
Step 2:-create a new folder “ansible-project” using command
Step 3: 
a)	> cd ansible-project	
b)	> nano inventory
c)	> write a private IP of “Ansible-server1” into inventory
d)	> write a private IP of “Ansible-server2” into inventory
e)	> write a private IP of “Ansible-server3” into inventory







f)	Save and exit

Task: Install Nginx and Start Nginx
Step 1: Create a new file called “first-playbook.yml”
 
Code:










 
Execute the playbook by using command:
ansible-playbook -i inventory first-playbook.yml
 

Output:
 
Verify the output:
Step 1: connect to any ansible-server1
Step run the command: sudo systemctl status nginx
 

