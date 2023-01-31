![](https://img.shields.io/badge/AWS-LAB-red)
## Expertise level practical learning for TOP-25 AWS services. 
Author: </br>![](https://img.shields.io/badge/RAKESH-KUBENDRAN.CHINNA-green)

**TOP 25 SERVICES:** 
- [EC2](#id-EC2)
- [VPC](#id-VPC)
- [Lambda](#id-Lambda)
- [Route 53](#id-Route53)
- [Glacier](#id-Glacier)
- [Cloud Front](#id-CloudFront)
- [RDS](#id-RDS)
- [Dynamo DB](#id-DynamoDB)
- [IAM](#id-IAM)
- [API Gateway](#id-APIGateway)
- [Cloud Watch](#id-CloudWatch)
- [Trusted Adviser](#id-TrustedAdviser)
- [EFS](#id-EFS)
- [SNS](#id-SNS)
- [Light sail](#id-Lightsail)
- [Certificate Manager](#id-CertificateManager)
- [KMS](#id-KMS)
- [S3](#id-S3)
- [Cloud Trail](#id-CloudTrail)
- [System Manager](#id-SystemManager)
- [Inspector](#id-Inspector)
- [Secrets Manager](#id-SecretsManager)
- [Cloud Formation](#id-CloudFormation)
- [EBS](#id-EBS)
- [Cost Explorer](#id-CostExplorer)

***

<div id='id-EC2'/>
<h2>EC2:</h2>
Before get into EC2. Let's understand what is virtualization and Hypervisor.
<br>
<strong>Virtualization:</strong>
<br>
Virtualization in computing is the process of simulating hardware and software in a virtual(software) env. 
<br>
<strong>Hypervisor:</strong>
<br>
The Software that creates and runs the virtualization is called a hypervisor. Two types of hypervisors are available in the market. 
Refer the below Image:

   ![](https://networkinterview.com/wp-content/uploads/2019/12/hypervisor.jpg)

<strong>EC2 is a webservice which aims to make life easier for developers by providing secure and resizable compute capacity in the cloud.</strong>
<br>
IT mainly consists in the capability of:
<br>
 1.Renting virtual machines(EC2)<br>
 2.Storing datas on virtual drive(EBS)<br>
 3.Distributing load accross machines (ELB)<br>
 4.Scaling the services using an auto-scaling group (AGS)<br>

<strong> PRACTICALLY WE WILL SEE HERE HOW TO CREATE EC2-INSTANCE</strong>

1. First select your desired region and click the Instances.
   ![image](https://user-images.githubusercontent.com/122355244/214496410-7642730d-de0a-49a6-b848-de93f73f2348.png)
2.Select launch instance:
   ![image](https://user-images.githubusercontent.com/122355244/214496718-0ab9f39f-b806-42dc-b375-93fabbdee5fa.png)
3. Provide the name and tags:
   ![image](https://user-images.githubusercontent.com/122355244/214496967-e46d22cd-c958-4cd2-8c74-ff125a0103b1.png)
4. Select the AMI type. For My case i have selected the AMAZON ec2-free tier.<br>
   ![image](https://user-images.githubusercontent.com/122355244/214497242-bb79729b-b772-4c0a-aa05-104183040e89.png)
5. Select the instance type.<br>
   ![image](https://user-images.githubusercontent.com/122355244/214497475-3f9012ae-36f0-4ef4-a230-b6c7e6cb73a1.png)
6. Create key pair.<br>
   ![image](https://user-images.githubusercontent.com/122355244/214497548-36fa53f2-074c-4218-ba7c-51ee2bb831d6.png)
7. Create Security.<br>
   ![image](https://user-images.githubusercontent.com/122355244/214497718-6ce210fe-462a-4085-83fd-29b36888c767.png)
 <br> 
 <strong>Note: You can select any other secuirty group also if its available. In this case we are creating new SG group.</strong>
 
8.Will see fruther about firewall rules detailed in firewall section seperatly. As of now everything is default.
   ![image](https://user-images.githubusercontent.com/122355244/214498138-025840dc-1a4b-4d55-ba65-ae09d0a517c7.png)

9.Select Volume Type
<br>
   ![image](https://user-images.githubusercontent.com/122355244/214498198-6967edd1-9a66-4366-bbbf-0a5d22e1c503.png)
<br>
10. Now launch the instance.<br>
   ![image](https://user-images.githubusercontent.com/122355244/214498425-0cd2f0fe-ddca-46a5-8aa0-fa4d8bb9d72b.png)
11. Provisioned instance will be available in the GUI.
   ![image](https://user-images.githubusercontent.com/122355244/214501518-096bc437-a912-476e-8c81-344893c97ed0.png)<br>

<strong>CONNECTING INSTANCE WITH PUTTY</STRONG>

1. Be handy with .ppk file and open the putty.
2. Before connecting to instance. Import the PPK file in putty.

   ![image](https://user-images.githubusercontent.com/122355244/214504262-66a11957-f0f8-4588-8f0d-0d654c4d4b42.png)

3. sucessfully connecting with instance with putty through public ip.
   ![image](https://user-images.githubusercontent.com/122355244/214504777-5c8b24ac-999d-4093-9f66-8dd0ad4ec33b.png)


<strong>EC2-instance-states</strong>
1. START - To start the stopped instance. <br>
2. STOP -  To stop the running instance. <br>
3. HIBERNATE - when you start up the instance, you're back to where you left off.<br>
4. TERMINATE PROTECTION - To prevent your instance from being accidentally terminated using Amazon EC2, you can enable termination protection for the instance.<br>

<strong>ENABLING HIBERNATE FOR THE INSTANCE </strong> 

Follow the Link: [HIBERNATE](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/enabling-hibernation.html)

<strong>TERMINATE PROTECTION</strong>

Select_instance -> click action-> instance settings-> change terminate protection and click enable.

    ![image](https://user-images.githubusercontent.com/122355244/214742070-b1375898-d9e6-436e-a55f-260a49ea2904.png)

    ![image](https://user-images.githubusercontent.com/122355244/214742191-0a30dd9c-3ccb-4531-9de3-78c37e8f882a.png)

<strong>EC2-INSTANCE TYPES</strong>
    ![image](https://user-images.githubusercontent.com/122355244/214745273-386ac321-2aed-49ab-8e99-90361ea41b9e.png)

Steps to change EC2 instance type:

1. Stop the instance
2. Select instance -> Action -> Instance settings -> change instance type.
   ![image](https://user-images.githubusercontent.com/122355244/214747896-1101d548-6058-406f-b640-3f8fd45ce9e5.png)<br>
 
   ![image](https://user-images.githubusercontent.com/122355244/214748733-55764f75-0304-4e15-ac46-8c63d7de687e.png)



***

<div id='id-VPC'/>
<h2>VPC:</h2>
<strong>what is VPC ?</strong> <br>
VPC provides us the private space that is required inside aws where we can define our own network and also use all the services of AWS. As per our requirement. <br>
Techincal explanation: AWS VPC lets you provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define.

<strong>Why VPC ? </strong>
 
The 3 most essential benefits you get from a VPC are privacy, security and prevention from loss of proprierty data.

   ![image](https://user-images.githubusercontent.com/122355244/214985993-6bd5c57d-98c8-4451-909a-6e50bebc9b8f.png)

<strong> COMPONENTS OF VPC </strong> 

1. Internet Gateway & NAT - It logically enables routing of traffics in the public network.
2. DNS: Standard which resolve names used over the internet into IP address. 
3. Elastic Ip: Its a static Ip which never changes.
4. VPC Endpoints: Private connection between your VPC and other AWS services without using internet.
5. Network Interface: A point of connection between a public and a private network.
6. Egress only IG: Allows only outbound communication from EC2 over IPV6
7. Route Tables: Defines how traffic is route between each subnet.
8. VPC Peering: Connections between VPC's

<strong>CREATING CUSTOM VPC THROUGH AWS CONSOLE:</strong>

1. Select Region
2. VPC_layer: Allows you to create custom network topology and custom network configuration for your ec2-instance based on your appliaction needs.
3. Network range of the VPC.
4. Availability Zone.
5. Subnet:<br>
          1. A subnet is a range of IP addresses in your VPC. <br>
          2. Network range of the subnet should be within the range of the VPC.<br>
          3. Subnet can be associated with only one Avilability zone.Once the subnet is created need to define the network ACl.<br>
          4. One-subent have only one NETWORK ACL.<br>
          5. Network ACL is the Network Firewall which is having INBOUND AND OUTBOUND rules.<br>
6. Security Group: Will work at ec2-instance level. All the inbound and out bound traffic to your ec2-instance passing your security group.<br>
    Deploy the EC2-instance in the selected subnet. When you deployed the EC2-instance on a specified subnet. AWS will automatically allocate a avilable IP address in     the subnet range and AWS crate a default ROUTE TABLE. <br>
7. Route tables are associated with subnets.<br>
   - 7.1 One subnet have only one route table.<br>
8. Create internet gateway associated with the VPC.

<strong>Refer the snapshot</strong>
     ![image](https://user-images.githubusercontent.com/122355244/214994296-9a5cab24-9b24-41be-bc71-ba7e7ccd0422.png)

<strong>STEPS TO CREATE TO CUSTOM VPC</strong>
 
 1. In search panel type VPC and browse.
     ![image](https://user-images.githubusercontent.com/122355244/215366834-b458f80a-74cb-4132-b112-b2afe10c44ef.png) <br>
 2. Create VPC<br>
     ![image](https://user-images.githubusercontent.com/122355244/215366877-707985c4-283c-4bb1-ae76-38c775e742cd.png)

 3. Select VPC only and provide your name tag.<br>
     ![image](https://user-images.githubusercontent.com/122355244/215368362-7c4e425b-074c-416e-8948-fa112d73579e.png)

 4. specify your IPV4 CIDR.<br>
    Short note for what is CIDR and how to calculate:<br>
    Using CIDR block we can define IP address pattern along with that we can also can decide how many address will need inside this VPC.<br>

   <strong>Inside CIDR portion we have two portions.</strong><br>
         1. Network portion
         2. Host portion

   172.31.0.0/24

   when we say 24 which is equalent to 3 octats

   172.31.0 -> This is allocated to network portion.

   Remaning 0 -> This is alloacted to host portion.
   
   Note: Each octat is 8 bits.

   Network portion 24

   Host portion - 8 

   2^8 = 256

   we will get 256 IP'S inside the VPC.

  Use below link for quick calculation.

  [CIDR CALCULATION](https://mxtoolbox.com/subnetcalculator.aspx)
  
  
  <strong>Break VPC into 2 subnets</strong>

   Subnet 1 (128)
   172.31.0.0/25
   Network Portion - 25
   Host Portion    - 7 

   Subnet 2 (128)
   172.31.0.0/25
   Network Portion - 25
   Host Portion    - 7 

  4. Sucessfully created VPC.
       ![image](https://user-images.githubusercontent.com/122355244/215370042-41b22d1f-5786-41b2-9bae-7779a41ddd4f.png) <br>
  5. Once VPC got successfully created. we need to create subnet.<br>
       ![image](https://user-images.githubusercontent.com/122355244/215370347-7fcc4f59-606c-48cb-a077-32aaa9bb752d.png) <br>
  6. Refer the below snap shot.<br>
       ![image](https://user-images.githubusercontent.com/122355244/215370853-a14f1d5d-3fca-4683-bbcb-22968cf560b2.png) <br>
       ![image](https://user-images.githubusercontent.com/122355244/215370945-41a8ef49-f19e-4e62-a11c-6ab2b4901bd2.png) <br>
  7. Create Route table:
      If you refer the below route table. Already one route table creeated for your VPC. That is called main route table. Main route table automatically get created by your VPC.
       ![image](https://user-images.githubusercontent.com/122355244/215372736-befc91d1-f8c0-479d-92ab-679436b1cfa6.png)
      When you click on the routes. It has one entry stating that all the traffic should go through the local gateway if the destination falling under the VPC range.         If you want you can create custom route table. 
       
       <strong>CREATE CUSTOM ROUTE TABLE:</strong>
       
       ![image](https://user-images.githubusercontent.com/122355244/215373626-0993cb91-eabb-4cb0-b823-24b421ef8e5f.png) <br>
       Specify your VPC and create route table.
       ![image](https://user-images.githubusercontent.com/122355244/215373845-91070d17-2c6a-4f9d-be98-12040238b078.png)<br>
       ![image](https://user-images.githubusercontent.com/122355244/215373903-697d384a-0c0b-4ab3-a6d7-6b6741ad76ef.png)<br>
        
  8. Once the Route table is created. Add the subnet to the route table which you created in the second step.<br>
       ![image](https://user-images.githubusercontent.com/122355244/215733349-406e04da-e770-45f7-9f04-8a242d115c6a.png)<br>
       ![image](https://user-images.githubusercontent.com/122355244/215733877-b392bbe5-55d1-40e2-a6c5-3b79b8ed3303.png)<br>
  9. Now, create Internet gateway for your VPC.<br>
       ![image](https://user-images.githubusercontent.com/122355244/215734304-9721ed3e-da33-488d-bac1-bf2edde21bb0.png)<br>
       ![image](https://user-images.githubusercontent.com/122355244/215735118-a6ecdd37-23e4-43f8-b9f9-d00468067b60.png)<br>
 10. Once the Internet gateway attach to your VPC<br>
       ![image](https://user-images.githubusercontent.com/122355244/215735685-9d94f92c-ef33-4674-afef-ced16c95e158.png)<br>
 11. Now add theInternet gateway to your route table.
       ![image](https://user-images.githubusercontent.com/122355244/215736369-36998f1a-9f33-410f-8d49-039646183a0e.png)<br>
       ![image](https://user-images.githubusercontent.com/122355244/215736665-810a4d37-5a9c-4366-a3a5-9ed0809ccdce.png)<br>
     Note: 0.0.0.0/0. Allows inbound HTTP access from any IPv4 address. TCP. 6. 443 (HTTPS)

  <strong> Test your VPC through provisioning new instance</strong>
  Note: You have the VPC and subnet which you have created not the default one.<br>
  ![image](https://user-images.githubusercontent.com/122355244/215737727-e9295066-3ab6-4702-bebc-1f1704c685e7.png)
  
<strong>Private Subnet vs Public subnet</strong> <br>
   
<strong>Public Subnet</strong>: A public subnet is a subnet that is associated with a route table that has a route to an Internet gateway. This connects the VPC to the Internet and to other AWS services.   

<strong>Private Subnet</strong>: A private subnet is a subnet that is associated with a route table that doesn’t have a route to an internet gateway. Instances in the private subnet are backend servers they don’t accept the traffic from the internet. 
  
<strong>Why Public Subnet</strong> ? 
The resources in the public subnet can send outbound traffic directly to the Internet and vice versa. For example web server needs to be accessed by users from the internet.   

<strong>Why Private Subnet ?</strong> 

Resources like database may require connection to internet for updates/patches but should not be accepting request from the internet. In such cases a private subnet is to be used.

<strong>Private Subnet vs Public subnet(LAB)</strong> <br>

In this lab we will create one ec-2 instance with public subnet and one ec-2 instance with private subnet then we will see the configuration required at the route-table level to have access to the priavte ec2 instance and see how to login to the private ec-2 instacne via th bastion host. 

Bastion host: A bastion host is a server whose purpose is to provide access to a private network from an external network, such as the Internet

Heading over to the AWS console to deploy the VPC architecture.
1. Create a vpc
2. Create a subnet(public)
3. Create custom route table.
4. Create a Internet gateway
   
(Already coverd in the previous lab (public).<br>

 1. create a new subnet (private)
 2. create a custom route table.
 3. create and deploy the ec2-instance in private subnet. 
 4. Try to connect the server but you won't because you have create the EC2-instance in private subnet.

In order to login to the private ec-2 instance you must have a public server. 

Already have a public server. trying to take SSH from the public server.<br>
![image](https://user-images.githubusercontent.com/122355244/215827293-327d4f0d-135a-40de-ae64-0d4feb3d57c2.png)

As you notice. permission is denied. In this case you have to take ssh with the pem key. (Mycase i'm using one key for all the server provisioning)

Make sure you have 600 permision for your key(security reasons)

![image](https://user-images.githubusercontent.com/122355244/215828848-80439040-1f5e-46cd-9dac-c1f717da7e0a.png)

successfully connected to the private ec-2 instance. 

In future if you want to install any rpm files or update the files you need internet access. As we metioned this a private instance you will not have a internt access. 

but by using the NAT connection. we can achieve this. 

Create a NAT gateway. 

![image](https://user-images.githubusercontent.com/122355244/215830671-93e807f7-044c-42dc-abb2-358c9a728e2e.png)

![image](https://user-images.githubusercontent.com/122355244/215831329-3126ddf5-fb06-4113-a95e-ba0984d7228a.png)

Once the NAT-Gateway is created headover to the routet tables and the routes accrodingly. select the route table which is associated with your private subnet.

![image](https://user-images.githubusercontent.com/122355244/215836739-fecf62e6-c94a-4826-918d-6ce67b1709d8.png)

Specifiy that by default the network traffic should go the NAT-gateway if the destination is not falling under the VPC range. Hence select 0.0.0.0/0






<div id='id-VPC'/>
<div id='id-Lambda'/>
<div id='id-Route53'/>
<div id='id-Glacier'/>
<div id='id-CloudFront'/>
<div id='id-RDS'/>
<div id='id-DynamoDB'/>
<div id='id-IAM'/>
<div id='id-APIGateway'/>
<div id='id-CloudWatch'/>
<div id='id-TrustedAdviser'/>
<div id='id-EFS'/>
<div id='id-SNS'/>
<div id='id-Lightsail'/>
<div id='id-CertificateManager'/>
<div id='id-KMS'/>
<div id='id-S3'/>
<div id='id-CloudTrail'/>
<div id='id-SystemManager'/>
<div id='id-Inspector'/>
<div id='id-SecretsManager'/>
<div id='id-CloudFormation'/>
<div id='id-EBS'/>
<div id='id-CostExplorer'/>
