# Building-an-Amazon-Virtual-Private-Cloud-VPC-Empowering-Secure-and-Scalable-Infrastructure-with-AWS

![ScreenShot](https://github.com/NavarroAlexKU/Building-an-Amazon-Virtual-Private-Cloud-VPC-Empowering-Secure-and-Scalable-Infrastructure-with-AWS/blob/main/Network-diagram.png?raw=true)

## Author:
Alex Navarro - Senior Business Intelligence Engineer

## 🔗 Contact Information
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/alexnavarro2/)
[![Email](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](https://mail.google.com/mail/u/0/#inbox?compose=GTvVlcSBpRjxKKJtxTLNxwpsKvpfbRSRnRLcTQRMZLcKCNfrJjXfcNNKPmstkbHJpzHGNZnHvhCph)

## Project Overview:
Build a VPC that includes a web server and an Amazon RDS database. Once both are created, connect the address book application running the web server to the Amazon RDS for MySQL instance. Upon successful configuration of the address book application with the RDS instance, we will be able to add and remove contacts from the address book.

## What is Amazon VPC?
https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html

## What is a Classless Inter-Domain Routing "CIDR"?
The CIDR block represents the IP address range that I can assign to my VPC. It specifies the network address and the number of significant bits used for routing within that network. It enables resources in my the VPC to communicate with each other, and with resources over the internet.

https://docs.aws.amazon.com/vpc/latest/userguide/vpc-ip-addressing.html

### Create a VPC:
* Go to the VPC management console
* Create VPC
* Choose VPC Only
* Give VPC Name
* IPv4 CIDR Block = 10.0.0.0/16
* Click Create VPC:

![Alt text](image.png)

We can see that my VPC has been created and now we can see the details configured for this specific VPC:

![Alt text](image-1.png)

### Create Public Subnet:
Remember that public subnets allow our vpc to talk to the internet. Therefore, we need to make sure that our public subnet has a internet gateawy and auto assigned public IPv4 or IPv6. We also will need to create a public subnet routing table.

* Choose Create Subnet
* VPC ID = My VPC
* Subnet Name = Public 1
* AZ = Select first AZ
* IPv4 CIDR Block = 10.0.1.0/24

We can see the subnet has been created and shows the configuration details mentioned above:
![Alt text](image-2.png)