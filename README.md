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

1. Copy the public key and open the putty.
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
VPC provides us the private space that is required inside aws where we can define our own network and also use all the services of AWS. As per our requirement.

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
