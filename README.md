# AWS-Web-Application 

Web Infrastructure for Smartshop 

log in on Aws as an IAm user Changed my region to Ireland as instructed on the project document 

## VPC Creation 

I tried creating a VPC but got the error code that number of vpc creation has been exceeded, below is an image of the error code.
![Vpc image](/Vpcerror.png)
Lita created a VPC, the public and private subnet, and the route table for everyone to use which means i no longer need to create a new VPC in ireland region sitting in one availability zone, below is the image of the VPC, public and private subnets,internet gateway, routetable.
### LITA_PROJECT VPC 
![Vpc image](/VPCLita.png)
### LITA PROJECT PUBLIC subnet
![subnet image](/PublicSUbnet_Lita.png)
### LITA PROJECT PRIVATE subnet
![subnet image](/PrivateSubnet_Lita.png)
### LITA INTERNET gateway
![Igw image](/IGW.png)
### LITA PROJECT ROUTE table
![routetable image](/RouteTable_Lita.png)

## Security group Creation 
Step 1: Named my security group Oyindamolaadewole_Lita  
Step 2: description is to allow SSH & HTTP traffic which means to enable communictaion between the VPC and the internet  
Step 3:  i selected the LIta Ptoject VPC  
Step 4: Created an inbound rule to allow ssh & http anywhere-IPV4 
Step 5: Created an outbound rule to allow all traffic  
Step 6:  I clicked on create, and then my security group was created 
Bewlow is the image of the security group, inbound rule and outbound rule.

### SECURITY group
![security group image](/SecurityGroup.png)
### INBOUND rule
![inbound rule image](/InboundRule.png)
### OUTBOUND rule
![outbound rule image](/Outboundrule.png)
 
## EC2 Instance launch 

Step 1: I created a key pair first then downloaded the .pem file  
Step 2: Search for Instances 
Step 3: I clicked on Launch Instance 
Step 4: Named my instance oyindamolaadewole_LitaEC2 
Step 5: clicked on the Amazon linux 2 AMI for the machine Image and the OS  
Step 6: Cliked on  the t2.micro from the instance family which comes with 1vcpu and 1Gib memory 
Step 7: included the keypair i created 
Step 8: scrolled to the network settings 
Step 9: attached the VPC created by lita 
Step 10: Attached a public subnet to the instance 
Step 11: I enabled public IPV4 
Step 12: attached the security group i created 
Step 13: I left the storage ta 8G as instructed 
Step 14: Confirmed my configuration 
Step 15: Clicked on Launch 

Instance public IP 34.253.236.134, below is an image of my EC2
### EC2 Instance
![Ec2 image](/EC2.png)
![Ec2 image](/EC2complete.png)

## Apache Attachment 
Step 1: Opened my instance 
Step 2: Clicked on connect 
Step 3: COnnected my instance 
Step 4: Clicked on the SSH Client
Step 5: Copied my keypair name and description which had already been combined by aws used as an example 
Step 6: went to my local machine, clicked on the folder i had saved my downloaded keypair 
Step 7: right clicked an empty space on an empty space and clicked on git bash 
Step 8: run my keypair code on the git bash terminal to ensure my keypair is not publicly visible 
Step 9:  i run the apache code to attache apache to my instace 
sudo yum update -y  
sudo yum install httpd -y  
sudo systemctl start httpd 
sudo systemctl enable httpd 

### GIT bash
![kaypair image](/Kaypaircommand.png)

Step 10: After running the code, i was able to attach my apache sucessfully

### Apache Test page
[Apache Image](/Apache.png)
  



