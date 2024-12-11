# AWS-Web-Application 

Web Infrastructure for Smartshop 

log in on Aws as an IAm user Changed my region to Ireland as instructed on the project document 

## VPC Creation 

I tried creating a VPC but got the error code that number of vpc creation has been exceeded.  
![Vpc image](/Vpcerror.png)
Lita created a VPC, the public and private subnet, and the route table for everyone to use which means i no longer need to create a new VPC. 
 

 

## Security group Creation 

Step 1: Named my security group Oyindamolaadewole_Lita  
Step 2: description is to allow SSH & HTTP traffic which means to enable communictaion between the VPC and the internet  
Step 3:  i selected the LIta Ptoject VPC  
Step 4: Created an inbound rule to allow ssh & http anywhere-IPV4 
Step 5: Created an outbound rule to allow all traffic  
Step 6:  I clicked on create, and then my security group was created 

 
 

## EC2 Instance launch 

Step 1: I created a key pair first then downloaded the .pem file  
Step 2: Search for Instances 
Step 3: i clicked on Launch Instance 
Step 4: named my instance oyindamolaadewole_LitaEC2 
Step 5:  clicked on the Amazon linux 2 AMI for the machine Image and the OS  
Step 6: Cliked on  the t2.micro from the instance family which comes with 1vcpu and 1Gib memory 
Step 7:  included the keypair i created 
Step 8: scrolled to the network settings 
Step 9: attached the VPC created by lita 
Step 10: Attached a public subnet to the instance 
Step 11: I enabled public IPV4 
Step 12: attached the security group i created 
Step 13: I left the storage ta 8G as instructed 
Step 14: Confirmed my configuration 
Step 15: Clicked on Launch 

Instance public IP 34.253.236.134 

 

## Apache Attachment 

Step 1: Opened my instance 
Step 2: Clicked on connect 
Step 3: COnnected my instance
Step 4: Clicked on the SSH 
Step 5: Copied my keypair name and description which had already been combined by aws used as an example 
Step 6: went to my local machine, clicked on the folder i had saved my downloaded keypair 
Step 7: right clicked an empty space on an empty space and clicked on git bash 
Step 8: run my keypair code on the git bash terminal to ensure my keypair is not publicly visible 
Step 9:  i run the apache code to attache apache to my instace 
sudo yum update -y  
sudo yum install httpd -y  
sudo systemctl start httpd 
sudo systemctl enable httpd 

Step 10: After running the code, i was able to attach my apache sucessfully 



# GIT HUB ACCOUNT SET-UP
Step 1: I clicked on GitHub which took me to the web github page
Step 2: I clicked on sign-up and followed the instruction to creat ACCOUNT
Step 3: I created a repository and enable README file and set it to public to enable access to my repo by others
Step 4: named the file AWS-Web-Application
Step 6: I downloaded git suitable for my OS on my laptop
Step 7: Installed the git
Step 8: i opened the Command line terminal on my laptop
step 9: run the git --version code to be sure i have successfully installed git

## Cloning repository
Step 1: Copied my repo link
Step 2: paste it on my cli
Step 3: run the command "git clone https://github.com/Banikale/AWS-Web-Application.git
step 4: successfully cloned my reposioty on my local machine

## Documentation
Step 1: downloaded notepad ++ to access my README file
Step 2: documented of my project process
step 3: save the document
step 4: opened my cli
Step 5: run the command "git status" to check the changes
step 6: run the command "git add ." to add the changes
step 7: run the command "git commit -m" to commit the changes
step 8: run the command "git push" to push it to my online git hub"

