Accessing-VM-Using-Cloud NAT

Problem: 
   To make the private instance created without external ip communicate with the internet using cloud NAT.



Purpose:
   Accessing VM instance and communicating with internet using cloud NAT without external ip.

Overview:
   The cloud Nat will allow the VM instance which is created in the private subnet to communicate with the internet without external ip and the VM instance which is created  in the public subnet can communicate directly with the internet because it has the external ip.

Required resources:
1)	  A VPC network with public and private subnet.
2)	  A firewall
3)	Two instances one with external ip and other without external ip
4)	Cloud NAT to access VM and communicate with internet
5)	Cloud Router
6)	Google compute address

Prerequistes:
          Terraform
         Access to GCP project

Steps:
1)	Create a vpc 
2)	Create two subnets one public and the other one private
3)	Create two instances one in each subnet, one with external ip and other one without external ip
4)	Create a firewall rule to access ssh
5)	Create a google compute address and a cloud router 
6)	Create Cloud NAT which should be created in the same region as that of private subnet region to make the instance which is created in the private subnet to communicate with internet without external ip.

Deployment:
	Clone the repo in terraform directory
	Then initialize terraform build using command
-	> terraform init
Now after build validate code by running cpmmand
-	> terraform validate
Upon successful validation verify deployment plan using command
-	> terraform plan
Now to deploy the resources run command
-	> terraform apply

