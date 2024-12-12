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




