![](https://img.shields.io/badge/AWS-LAB-red)
## Expertise level practical learning for TOP-25 AWS services. 
Author: </br>![](https://img.shields.io/badge/RAKESH-KUBENDRAN.CHINNA-green)

**TOP 25 SERVICES:** 
- [EC2](#id-EC2)
- [AdvanceEC2 Concepts](#id-AEC2)
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

![image](https://user-images.githubusercontent.com/122355244/215836739-fecf62e6-c94a-4826-918d-6ce67b1709d8.png) <br>

![image](https://user-images.githubusercontent.com/122355244/215837684-33312b5f-ac33-490d-91a9-f8cf585f9d11.png)


Specifiy that by default the network traffic should go the NAT-gateway if the destination is not falling under the VPC range. Hence select 0.0.0.0/0

Post this check try to ping google or try to install any pakagesin the private subnet instance to validate.  

<div id='id-AEC2'/>
<strong>EC2-ADVANCE_CONCEPT</strong>

1. <strong>EC2-Instance_Meta_data-retrival.</strong> 

   execute the below URL end point to retrive the AWS EC2-META DATA.
   
   curl http://169.254.169.254/latest/meta-data/
   
   ![image](https://user-images.githubusercontent.com/122355244/216750239-6b1da164-8521-4d03-9433-f556f12025ed.png)
   
2. <strong>Bootstrap EC2-instance:</strong>

     What is Bootstrap?
      Installing your application, dependencies, or customizations whenever an Amazon EC2 instance is launched.
      
     while provisioning EC2-instance, In Advance details section you can find the USER DATA-OPTIONAL, here you can provide your command on the user data section.
     
     ![image](https://user-images.githubusercontent.com/122355244/216750458-433b631f-e62d-4577-8b2b-42005ad01c41.png)
     ![image](https://user-images.githubusercontent.com/122355244/216750479-8a3156b2-168c-41bc-ad6f-13d0876b867d.png)

     In my case, I'm installing  apache. here is my code. below commands will be executed at the time of ec2 instance is launched. 
     
     "#!/bin/bash <br>
      yum update -y <br>
      yum install -y httpd.x86_64 <br>
      systemctl start httpd.service <br>
      systemctl enable httpd.service <br>
      echo “TEST PAGE BY RRAKESH KUBER from $(hostname -f)” > /var/www/html/index.html"
      
    ![image](https://user-images.githubusercontent.com/122355244/216750654-02d9aef8-dea1-442e-86ad-c2aba4156971.png)
    
    Copy your public IP and open it in chrome. (Make sure you have opend port 80 in your security group)
    
    ![image](https://user-images.githubusercontent.com/122355244/216751092-2c9f57df-ec7f-4a55-a6f0-f97c9a28bbe1.png)
    
    Successfully you have installed your apache service at the time of EC2-instance launch. You can check the get system log to see the user data action.
    
    Get system log:
    
    ![image](https://user-images.githubusercontent.com/122355244/216751224-2012a8ec-c546-455d-a173-ef3335e37581.png)

    Cloud-init is executing the command provided in the user data.
    
  3. <strong>AMI-CREATE,COPY AND MANAGE PERMISSIONS: </strong>
     what is AMI ?
     
     AMI is a template which contains OS and other related softwares. You can select your AMI at the time of EC2-instance launch.
     
     ![image](https://user-images.githubusercontent.com/122355244/216751716-f2d85540-3a4e-4714-b6b1-956d8e00c2eb.png)
     ![image](https://user-images.githubusercontent.com/122355244/216751779-754e7cb7-ba84-43a9-8a69-0d86c59ab53b.png)
  
     AMI market place will show you all the AMI's which are managed by the 3-rd party vendors. You can buy the AMI'S form the 3rd partyvendors and run in the AWS cloud.
    
   ![image](https://user-images.githubusercontent.com/122355244/216751854-d1c0360f-4a39-49f1-98ee-1828161de777.png)


   Coummunity AMI's ae created and managed by the different communities and provide access to the public.
 
 ![image](https://user-images.githubusercontent.com/122355244/216751951-a0ad17f5-69b0-46c8-b4e4-165ba0ed11bb.png)

    <strong>CREATE CUSTOM AMI</strong>
    
Let's say every organization is having certain configuration steps needs to be done on every EC-2 instacne  which is eployed on the AWS cloud. It'a tedious job to congfigure these configuration steps manually on  a every EC-2 instance. Once the server is lanuched. Hence you can deploy the EC2 instance by base AMI which is provided by the AWS. Then you can configure as per the bussiness needs. Then you can create a custom AMI from the running fully configured instance. So that the AMI which are creating will be fully packed with the required configuration as per the bussiness needs. 

In my case ec2-instance already configured as a webserver as per my org standards. 

Now we will go-head and create the AMI.

 To create a AMI select the instance go to actions. Click on Image&templates and create image. 
 
 ![image](https://user-images.githubusercontent.com/122355244/216752583-d19a599c-4c77-463a-8ed7-4c0e0fb0b8c7.png)
 
 ![image](https://user-images.githubusercontent.com/122355244/216752676-127d6336-4527-453e-b1cb-a1f3a53de5ff.png)
 ![image](https://user-images.githubusercontent.com/122355244/216752712-5835e61f-23d4-4261-981a-ca23b15702a8.png)

 
 Aws providing an option not to reboot the instance at the time AMI creation. Make sure you check the boxif its a production instance. 
 
 
 Under the image click on AMI.
 
 ![image](https://user-images.githubusercontent.com/122355244/216752773-75394898-eacd-414a-b882-889ecbbb361b.png)

 Once the AMI is in available state. We can use the AMI at the time launching the new instance. 
 
 under MY AMI's select your custom AMI.
 
 ![image](https://user-images.githubusercontent.com/122355244/216752921-a2cef0d5-85f7-4f20-b74e-4673be3f9916.png)

Now you can see the same webserver is live on new ec2-instance.
![image](https://user-images.githubusercontent.com/122355244/216753115-4cb33a73-c2cc-4152-ad40-7d8d99285c0c.png)

 when you have created the custom AMI. By default the AMI is a private. Means that AMI is accessible only in your account. In order to manage the permessions follow the below.
 
 Select the AMI and click the edit EMI permissions and make it public.
 
 ![image](https://user-images.githubusercontent.com/122355244/216753313-efb2d09e-2449-4076-9ec9-6ec38880d47d.png)

 
 ![image](https://user-images.githubusercontent.com/122355244/216753279-d6742d29-7ca6-4e10-831e-c878892e323c.png)

Higly recommanded only go with private. If the AMI consists any ORG level data.

Use you can share the AMI's with other Account trustable account as well.

![image](https://user-images.githubusercontent.com/122355244/216753383-d4810722-72fe-4643-936a-16b411339706.png)

Note: AMI'S are region specific. In order to copy AMI from one region to other region follow the below.

![image](https://user-images.githubusercontent.com/122355244/216753462-e973e469-fb37-4617-a912-894d81fa2b1e.png)

![image](https://user-images.githubusercontent.com/122355244/216753495-d32a0260-1d95-41a5-a662-2c0d98b6b999.png)

select the destination region. Now onwards your AMI will be available in your destination region. You can create a new instance with that AMI.  


<strong>EC2-PLACEMENT GROUPS</strong>

Currently AWS supporting below 3 placement groups.

1.Cluster
2.Partition
3.Spread

<strong>Cluster:</strong>: AWS is maintaing the pysical servers in racks and respective availabilyty zone. when you created a cluster placement group AWS will consider setup a racks in the cluser placement groups. then when you deploye  a ec2-instance in a cluster placment group. It enusre that all the servers will sharing the hardware from the set of racks consider in the placement group. 

<strong>Partition:</strong>: when you have created the partition group. Aws will ensure that multiple partitions are creatd in the availablity zone. As per the selection. Each partiton is created as a set of racks creatd as a partiton cluster.  when you are deploying the ec2-instanecs in the partition cluster. you need to specify the instacne should be get created in which partition. when you have choosen a partition as a partition1. servers will be created on the hardware which is consider as a partition 1

<strong>Spread:</strong> when you are deploying the instance in the spread placement groups.Aws will ensure that each instance is deployed into the set of racks created as a sperate cluster. 

Aws will ensure that single set of racks which is created as a cluster is not having multiple instances. One instance will deployed into one set of racks. 

Cluster placement group are more recommended for the applications which would required a low network latance and hig network throughput

Partition placement group are more recommended for the applications which are large distributed and replicated workloads between the EC2-instance. 

Spread placement group are more recommended for small number of critical instances that sholud be kept sperate from each others.

<strong>LOGIN TO PLACEMENT GROUPS TO SEE THE PLACEMNET GROUPS</strong>

![image](https://user-images.githubusercontent.com/122355244/216755426-f8e43e2b-70ae-4a86-944e-43b2438d5705.png)

specify the placement statergy:

![image](https://user-images.githubusercontent.com/122355244/216755545-a7a62efb-7a15-433b-9376-55a1497ff5e0.png)

Note: "A partition placement group can have a maximum of seven partitions per Availability Zone."

Select the partition group at the time of launching the instance.

![image](https://user-images.githubusercontent.com/122355244/216755738-c2feb5d7-048e-4a03-af08-3dc317d08ae2.png)

<strong> INSTANCE STORAGE VOLUMES</strong>'

Instance storage volumes- Hardware attached to EC2-instance.

                         - Data cannot be replicated by default
                         
                         - Not possible to take snapshot.
                         
The data which is stored in the Instance storage volume will not be persistance. 



<div id='id-VPC'/>
<div id='id-Lambda'/>
<div id='id-Route53'/>
<div id='id-Glacier'/>
<div id='id-CloudFront'/>
<div id='id-RDS'/>
<strong>WHAT IS RDS?</strong>

Let's say clinet is accessing the web application www.google.com.Then the web app must be host on the web app server. Clinet can initiate http request to the server to get the webpages. If the web appliaction is very static then application server itself enough to keep the appliaction related data and can start serving the data back to the clinets but if the web app dynamic in nature. The the appliaction server is not enough to keep the bussiness related data. Hence appliaction server would required database storage where the data can be saved. when we have separte ioslated database storage space then whatever data is uploded by the clinet that data will be saved in the database space. when the clinets would like to download the files. The data can be fetch from the data storge and given back to clinets. Database storage also can store the credentials of the users.


When clinets are making a request to the appliaction server.Either to upload the data or download the data. Then appication server would connect to the database storage. Hence appliaction server taking a help of RDBMS software will be MYSQL,POSTGRESQL,ORACEL,SQLSERVR.So that applaiction server can make a request to the database storage with the help RDBMS software.

In this architecture,

Application server is only installed and configured with the appliaction server software. Which can take the http request from the clinet. If the data access would be required application server connecting to the database and fetch the data. Its a tedious job to install and configure RDBMS software to work with the data base storage space. 

Hence, AWS introduced RDS service wich is the database solution over the cloud. When ever we are used RDS service to create database

It will comes with installed and configured with the required RDBMS software. 

<strong>RDS_LAB</strong>
1. Search in Console for RDS.
![image](https://user-images.githubusercontent.com/122355244/218349575-be24fe97-d09d-4c81-ac44-8a9e082e9473.png)
2. Create database.
![image](https://user-images.githubusercontent.com/122355244/218349754-08efbb5e-a687-4fc4-8ff3-0ed98983b4b4.png)
3. Select the database.
![image](https://user-images.githubusercontent.com/122355244/218349858-6a57dd89-db62-4b8b-a6d8-f8a49b704787.png)
4. Select MYSQL version and template name.
![image](https://user-images.githubusercontent.com/122355244/218350137-220ac91e-308a-4783-95c6-b8b293643a95.png)
5. specify the master password.
![image](https://user-images.githubusercontent.com/122355244/218350091-56111193-416b-4fbf-a373-8a5a68764d79.png)
6. specify the storage as per the bussiness needs. 
![image](https://user-images.githubusercontent.com/122355244/218350537-38488396-4499-41a6-98f8-1b3c7521dc01.png)
7. In connectivity section.Specify your VPC.
![image](https://user-images.githubusercontent.com/122355244/218351834-461b5da2-2a1d-4352-ba64-3ca21febfebe.png)
8. Successfully created Amazon RDS.
![image](https://user-images.githubusercontent.com/122355244/218354325-5e03f4a7-13f6-4638-acaa-2b745e51f890.png)


<div id='id-DynamoDB'/>
<strong>DynamoDB: Managed NOSQLDATABASE</strong>

1.create Dynamo DB table.

![image](https://user-images.githubusercontent.com/122355244/218354892-c21aafeb-6116-4946-ad0f-c70de5b22366.png)
2. DynamoDB is a schemaless database that requires only a table name and a primary key when you create the table.
3.![image](https://user-images.githubusercontent.com/122355244/218408729-0651afd9-4e4f-4e66-91b6-119c1066cb69.png)
4.![image](https://user-images.githubusercontent.com/122355244/218408869-a53f8d9e-ee93-4c48-a410-747f6abccd3a.png)



<div id='id-IAM'/>
<div id='id-APIGateway'/>
<strong>API gateway is used to build, deploy and manage API'S</strong>
   
Let's say we have deployed the application in the lambda function or in the EC2-instance. If it's streaming related data application then the application will deployed in the kinesis service and if its database solution you can even use dynamoDB or the appliaction might be installed and configured in any of AWS services as per the bussiness needs. 

At the end, all the applications will be deliver to the end customers.

End customer accessing the bussiness applications over the internet based on their needs. Some customer use the bussiness applaictionsonly to view the stats. some other customers also use the same bussiness appliaction to download the data. To overcome this, AWS has introduced API gateway.
   
When the client wants to access the applaiction. The request wil go through the API gateway. 
   
   <strong>API GATEWAY LAB SETUP</strong>
   
   1. Head over the AWS console and search for API GATEWAY.
   ![image](https://user-images.githubusercontent.com/122355244/218415634-e2349cc5-5fc9-4c13-9a4c-0e12b117c710.png)
   2. Choose the API. In my case i'have choosen the REST API.
   ![image](https://user-images.githubusercontent.com/122355244/218416382-601bc9e5-9742-4ffa-8f0c-bff6e57ab4ba.png)
   3. Choose the protocol.
   ![image](https://user-images.githubusercontent.com/122355244/218416782-024c9892-46ad-4daa-bc48-d90c428dc601.png)
   ![image](https://user-images.githubusercontent.com/122355244/218417435-07632f5b-8ee3-4e5d-8689-d4903322232d.png)
   4. API Got created.
   ![image](https://user-images.githubusercontent.com/122355244/218418144-2d41eb6a-45e6-4604-b9c8-f50e3f1c21c6.png)
   5. ![image](https://user-images.githubusercontent.com/122355244/218418740-27603d76-3985-40f4-9459-3522b5231a77.png)
   6. ![image](https://user-images.githubusercontent.com/122355244/218418974-a0b20d6e-4612-4391-9f28-31da3a81e751.png)
   7. ![image](https://user-images.githubusercontent.com/122355244/218419132-9611719f-2ad2-436f-9537-c0b892e0cb54.png)

   
<div id='id-CloudWatch'/>

<strong>what is cloud watch ?</strong>

Monitoring solution provided by the AWS to monitor the AWS resources. 

If any case you end up with any perfromance issue. You would be reqiured to see the utilization performance of RAM and PROCESSOR of the EC2-instance. Based on the utilization metrices you will be knowing to change the instance type to meet the bussiness requirements. The compenent which is  monitoring any AWS iscalled metrics. This metrics can be seen through clouddwatch.

![image](https://user-images.githubusercontent.com/122355244/217433684-20e01a5b-04d2-44b0-b6b0-2956206c5902.png)


Search for cloudwatch.

![image](https://user-images.githubusercontent.com/122355244/217434721-500e7901-9d18-4ad5-86b5-d88ac968b446.png)

Click on Metric. It will show you all available metrics. It will show you all the possible, available metrics for all various resourse created in the regions.

![image](https://user-images.githubusercontent.com/122355244/217435146-a8dc7797-f486-4407-8176-f12b3c74bc3d.png)

Click on EC2 and per instance metric.

![image](https://user-images.githubusercontent.com/122355244/217435857-e737a059-3ab2-4c56-916c-afa368cc0a32.png)

Filter based on your EC-2 instacne. It will show all the metrices currently available for the EC2-Instance.

![image](https://user-images.githubusercontent.com/122355244/217436108-b3f4273b-a600-4ad5-b229-cec7a4114932.png)

To see the CPU utlization click the cpu utilization.

![image](https://user-images.githubusercontent.com/122355244/217436496-c8f1b4aa-4218-46b4-bc86-a92ba7264f34.png)

![image](https://user-images.githubusercontent.com/122355244/217436527-56dc4464-0d3a-4643-af85-c28d750b9811.png)

![image](https://user-images.githubusercontent.com/122355244/217440416-c066fab2-2d34-4ce2-be3b-208feb429dc3.png)

<strong>create custom dashboard</strong>

![image](https://user-images.githubusercontent.com/122355244/217441645-a5aaf02d-acf7-49ad-a5ea-b9f4af24e7bc.png)

![image](https://user-images.githubusercontent.com/122355244/217441858-999c6dd7-d4e2-4355-9545-8b80abe42b4f.png)

Select Metrices:

![image](https://user-images.githubusercontent.com/122355244/217442137-59527e7e-12f5-4c31-8f14-d55abbb8f8ac.png)

![image](https://user-images.githubusercontent.com/122355244/217442304-6111a208-b018-48d6-ba8a-906b069890b9.png)

![image](https://user-images.githubusercontent.com/122355244/217442730-7689bc94-8b37-438c-9080-7d4bcddc8a1a.png)


successfully created your custom dash board.

![image](https://user-images.githubusercontent.com/122355244/217442504-8c456a1f-206c-4c83-854a-48e21082b371.png)

<strong>cloudwatch_Alarm</strong>



***

<div id='id-TrustedAdviser'/>
<div id='id-EFS'/>

<strong>What is EFS</strong>

AWS EFS service is used to setup and manage network file storage of EC2-instances.
Let's say you have multiple ec2-instancs created in differnt availaibilty zones. when you have installed and configured appliaction cluster on these ec2-instacne. This ec2-instance required a shared data access. when you configured application cluster. If one of the system is down other instance will contineou the services to the end customers. Hence all the instances which part of the appliaction cluster would require the same data access. AWS is introducing EFS service to provide shared data access to multiple instances and providing the integrity of the data when multiple ec2-instance accessing the data at the same time. 

EFS is region level service. EFS service is used by the multiple ec2-instances in a differnt availability zone to have the access to the same data. 

EFS CHARACTERISTICS:
  1. NETWORK FILE SYSTEM.
  2. EBS
  3. PAY AS YOU GO SERVICE.
  4. scale on demand. 

Once EFS service is created will be mounted in the multiple ec-2 instances. EFS will be createing mounted targets in the each and every availabilty zone through this mounted targets EFS can mounted locally in the EC-2 instances. 

EC-2 instacnes will be making a request through port 2049 as its a network file system. Hence the reason you to create security group for your EFS making sure 2049 is allowd in the inbound rules. Once the port access has been granted to EC-2 instaces. EFS file system can be mounted as a local file system in all the ec-2 instacnes which are part of the applaiction cluster. 


When you mounted EFS file system as local file system it will be mounted as /mnt in all the ec2-instacnes. Means the data which is stroed in EFS system will be access by all the systems which are part of the appliaction cluster.

<strong>CREATE EFS</strong>

1. First Allow the 2049 port for the EC2-instacne. For this we are creating a new security group. 
   ![image](https://user-images.githubusercontent.com/122355244/218233016-d88b789f-4b88-404e-a952-80538bd33d47.png)
   ![image](https://user-images.githubusercontent.com/122355244/218233049-8195828e-1b05-4cac-b909-ad7c4734a938.png)

2. Create EFS.
   ![image](https://user-images.githubusercontent.com/122355244/218296420-31128135-5acb-478f-a1c5-9733daa7d962.png)
   ![image](https://user-images.githubusercontent.com/122355244/218296465-cbe23d14-4ef4-4c99-98db-a11012b1a876.png)
   ![image](https://user-images.githubusercontent.com/122355244/218296497-0f7b66c5-7adb-4a4f-8e7c-f27a23e8d748.png)
3. Now attach the created EFS.
   ![image](https://user-images.githubusercontent.com/122355244/218296528-75ca0de5-c51a-4ab5-a19a-a7b29a9b1dea.png)
   ![image](https://user-images.githubusercontent.com/122355244/218296607-e1aad86d-3485-4615-a013-0b616088cfc3.png)



<div id='id-SNS'/>


***

<div id='id-Lightsail'/>
<div id='id-CertificateManager'/>

<strong>what is Certificate Mannager</strong>

Certificate manager service is used to provision, Manage,deploy and renew SSL and TLS certificate on AWS platform.

Lets get understanding data encryption and types.

1. Data encryption at Rest
2. Data encryption in transit


<strong>Create SLL/TSL certificate</strong>

Head over to the managment console and search for Certificate manager.

![image](https://user-images.githubusercontent.com/122355244/217505536-de249a2e-9b0a-4838-b0b6-62b265242bca.png)

specify the domain name:

![image](https://user-images.githubusercontent.com/122355244/217506131-9782988b-5c4c-461a-a36b-fa9787dfc2e0.png)


<div id='id-KMS'/>
<div id='id-S3'/>
<div id='id-CloudTrail'/>
<div id='id-SystemManager'/>
<div id='id-Inspector'/>
<strong>Amazon Inspector</strong>
Amazon Inspector: Used to analyze the application level security. AWS is provinding amazon which can scan the EC2-instance and report you if the ec2-instane is not configured as per the bussiness practices and it can be scanned of any vulnerablity can be identified.

Need to choose the assessment type.

Network Assessment and Host Assessment.

Network Asssessment - No agnet is required.
Host Assessment - Agnet must be install in the target instance. 

<strong>Setting up INSPECTOR Service </strong>

1. ![image](https://user-images.githubusercontent.com/122355244/218601637-b62ad05c-c015-4271-85c2-fc0284750027.png)<br>
2. ![image](https://user-images.githubusercontent.com/122355244/218601880-05a6967f-9d7a-4fcf-8506-7c6343628dd3.png)<br>
3. I'm using the kay_pair_name tag. Means that ec2-instances which are associated with key_pair_name that will consider as assessment target. <br>
4. ![image](https://user-images.githubusercontent.com/122355244/218607133-520d304e-758b-4062-90eb-a85b302b59cc.png)<br>
5. Preview the target,<br>
6. ![image](https://user-images.githubusercontent.com/122355244/218607868-bbb1c04d-90dd-402b-b585-f6bfb44279bf.png)<br>
7. Create assessment template.<br>
8. ![image](https://user-images.githubusercontent.com/122355244/218608700-89c5ef7e-8908-4ac3-8f96-8ce6546e4d2c.png)<br>
9. ![image](https://user-images.githubusercontent.com/122355244/218608834-bab6471a-b387-41e8-a7b4-53f5776c6382.png)<br>
10.![image](https://user-images.githubusercontent.com/122355244/218609010-9b44bfdd-9fb6-40a9-b22a-373811492e84.png)<br>
11. In Assessment Run. You will be able t download the report.<br>
13. ![image](https://user-images.githubusercontent.com/122355244/218609147-9e329aad-e008-44b5-8355-0190e23f38ab.png)


***

<div id='id-SecretsManager'/>
<strong>what is SecretsManager</strong>

AWS Secret Manager enables you to easily rotate, manage, and retrieve database credentials, API keys, and other secrets throughout their lifecycle.
It is one central location to keep all credentials secure.

![image](https://user-images.githubusercontent.com/122355244/218424544-8c165379-df1b-44f5-8f38-e30a5194c5bc.png)

1.Select the secret type.
![image](https://user-images.githubusercontent.com/122355244/218599290-44200843-df95-4075-ab9a-68f951b75aea.png)
2.Specifiy the secret name.
![image](https://user-images.githubusercontent.com/122355244/218599628-9725d7ba-d3fb-4c7a-9138-4c267f7bc321.png)
3. Successfully created the secret.
![image](https://user-images.githubusercontent.com/122355244/218599886-20e3a5dc-2b40-4315-857e-dc6c177d0c29.png)


<div id='id-CloudFormation'/>
<div id='id-EBS'/>

<strong>EBS</strong>

When you are launching a ec2 instance in any one  of the avilability zone by default one root volume get created and attached to the EC2-instacne.

Every ec2-instance has its own root EBS volume and its also possible to create additional volumess and attched to the ec2-instance.

 TWO TYPES OF VOLUMES CURRENTLY SUPPORTING BY AWS.
   1. EBS Volumes.
   2. Instance store Volumes. 
 <strong> EBS volume Types:</strong>

- General Purpose SSD(gp2)
- Provisioned IOPS SSD(io1)
- Throughput Optimized HDD(st1)
- Cloud HDD(sc1)
- Magnetic (standard)

<strong> EBS Volume Characteristics </strong>

- Persistent block storage volumes
- 99.999% availability
- Automatically replicated within its Availability Zone(AZ)
- Point in time Snapshoot support.
- Modify volume types as per the bussiness needs. 

Log in to the ec2 instance and type the command lsblk

![image](https://user-images.githubusercontent.com/122355244/217429622-d9010051-78af-4124-ab52-5d67eaad18f3.png)

you will see outupt xvda is attached to the current instance. 

xvda - os level nameing standards for your EBS volumes.

Will show you how to create one more ebs volume and attached to the same ec2-instance.

![image](https://user-images.githubusercontent.com/122355244/217430224-665fbaf8-6b32-43e5-a7a6-9ea244f72406.png)

Scroll down to the volumes and create volume.

![image](https://user-images.githubusercontent.com/122355244/217430330-def509e8-d29b-4354-a68b-47c667bd2b72.png)

![image](https://user-images.githubusercontent.com/122355244/217430462-478a6394-374d-4286-b3ef-f13d6359b3e0.png)
 
 Once the volume state is in available state attch to your ec2-instance.
 
 ![image](https://user-images.githubusercontent.com/122355244/217430923-056f6c1f-238e-459c-9841-864583712435.png)

 ![image](https://user-images.githubusercontent.com/122355244/217431326-d118fd52-4a47-48cc-a6b6-4bbe027e4ae3.png)
 
 Successfully attached the new EBS volume to the EC2-INSTANCE.
 
 ![image](https://user-images.githubusercontent.com/122355244/217431641-44e44f27-db69-4bcb-a8d4-9238474c5600.png)



<div id='id-CostExplorer'/>
