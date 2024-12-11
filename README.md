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


