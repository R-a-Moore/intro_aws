# Cloud Computing

![page 1](https://user-images.githubusercontent.com/47668244/185719157-2303a7e1-12e1-4891-9417-f4662fb34e39.png)

## Introduction

-	Cloud computing
-	Different models
-	Benefits, cons
-	AWS – global infrastructure

## What is Cloud Computing?

![page 2](https://user-images.githubusercontent.com/47668244/185719166-57311c6e-1478-4f0a-b0e4-bcc45cc973fc.png)

Let’s say you are a organisation looking to create a production environment for the software application that your team has developed. 
For this production environment, you want to be able to have:

-	High performance hardware. So it can complete tasks and execute the application in a timely manner 
-	Large volume / storage, for a vast array of data sets
-	Instance access
-	Scalability; you might want to later expand the use of this production environment to account for expanded versions of the application.

### Definition

![page 3](https://user-images.githubusercontent.com/47668244/185719178-eee943db-4c4c-4a70-86a4-580a2706733b.png)

Cloud computing refers to the delivery of on demand computing services, which provides a pay as you go structure.
In practice, this means that all of the computing infrastructure (hardware), processes, and applications are not located on site, but in an off-site environment dedicated to the delivery of those requirements.

### Deployment Models

Cloud computing has three methods of deployment
-	Public  - Cloud service Providers
-	Private – privately owned by organisation
-	Hybrid – amalgam of the two

## Pros

![page 4](https://user-images.githubusercontent.com/47668244/185719193-e3300680-312c-4e1f-8e00-f8e3bd3e4170.png)

Cloud computing provides a number of advantages to an organisation
-	Scalability – it is far easier and often cheaper to scale up your instances and number of environments via cloud computing. 
-	No technical maintenance and management concerns (both technical and security)
-	data security – as far as identity and access management is concerned, there is a separation between the cloud resources and the organisation’s infrastructure. only those maintaining and administrating the cloud resources have rights over it. So if one is breached, the ideally other remains secure.
-	robust disaster recovery systems – if your organisation does not have the redundant infrastructure and procedures to account for, and recover from disasters; be they natural, corporate, or security, cloud computing already provides that. In redundant machines, backup storage, and off-site separation as mentioned previously.

## Cons

![page 5](https://user-images.githubusercontent.com/47668244/185719200-9a4dffb8-6e36-4da5-b08a-93cf96cc49ce.png)

When going into cloud computing there are a number of key things to consider
-	resource dependencies – whilst you no longer have to worry about the maintenance and management of the infrastructure as you have handed it off to the cloud provider, this also means you no longer hold control over it. And as such, if the provider does not meat your requirements or you outgrow their capabilities, you will potentially have to change providers. 
-	downtime – cloud providers may grow overwhelmed by client requests (so private cloud service my be the desired model)
-	infrastructure requirements  – your organisation still needs the appropriate infrastructure to connect and run the cloud environment instance.
-	Security concerns – whilst there are benefits to the use of cloud computing in regards to security, it should also be noted that in regards to public cloud security, where cloud providers may be resourcing hundreds of organisations, if a breach occurs for them, a potential for adjacent organisations to also incur risks.

## Service Models

![page 6](https://user-images.githubusercontent.com/47668244/185719205-59a2e522-1c52-4c2b-be56-831c50e002bd.png)

-	IaaS (Infrastructure as a Service) – where only the hardware such as machine instances, networks, processes and storage is provisioned. Such level services require you as the organisation to decide and implement the operating system, instance firewalls and the higher-level applications and software to run on the machine. 
-	PaaS (Platform as a Service) – is where the hardware requirements are fulfilled, and the applications meant to provide facilities for tasks such as software development.
-	SaaS (Software as a Service) – where the entire machine has been provisioned with hardware, OS, applications and other peripherals such that you can begin working on it 


# Cloud Computing with AWS

![aws](https://yt3.ggpht.com/ytc/AMLnZu-TeqYTUHtz5NM4fN0RbWTETgl4L-HHzTWV5X7nAnU=s900-c-k-c0x00ffffff-no-rj)

Amazon Web Services (AWS), is the world's largest cloud computing service provider. Servicing over 200 fully featured services, which make up 67% of the world's cloud infrastructure.

AWS global infrastructure operates in 84 availability zones. And services millions of active customers, covering virtually every industry and enterprise - both public and private secotrs.

### Shopping - What Requirements do we look for when buying a machine?

- cpu
- display
- gpu
- ram - performance
- storage - called volume in cloud - peristant/non-volatile
- motherboard
- power
- security, firewalls etc

When making/buying a machine you have to decide upon the specification, the costs and benefits, the purposes, etc. 

When going onto the cloud, you negate all of the specific machine issues

## EC2

![ec2](https://sawadeeeen.com/wp-content/uploads/2020/09/EC2.jpg)

EC2 (elastic comput service) is one of AWS' services, which allows customers to rent virtual computers on which to operate their own applications. 

EC2 is the platform what we will use to make the machine we'd like to build based on our requirements to deploy on the cloud.

![EC2 instance on AWS](https://user-images.githubusercontent.com/47668244/185410403-d6784a4f-d98e-4bf4-ba29-39958cb70077.png)

Similar to our virtual machines we will build our machines with EC2 on AWS, using a very similar process. However, we will of course be setting it up outside our localhosts, needing to connect to the machine with an SSH key connection.

### Conventions & Practices

- AWS naming convention for services - `group_person_task` - for example - `eng122_Shahrukh_ec2`

- When not in use (09:00 - 18:00) terminate. It costs money to run. Ask if you want to run out of hours, so that it can be authorised.

- for the duration of this course ensure you are logged in in Ireland - `Europe (Ireland) eu-west-1`.

- Do not delete anyone else's services

- DO NOT share AWS account details or keys with anyone - so don't push them to github!!!

#### Security groups

when administrating security groups, you should name your security group relevant to it's role and your instance machine.

## Set Up

when selecting operating system (in this case) choose
Ubuntu Server 18.04 LTS (HVM), SSD Volume Type

### Start / Stop Instance

- select instance

![create a new EC2 instance](https://user-images.githubusercontent.com/47668244/185580673-d3de607a-e61f-4519-97ef-abe0e2f2cb83.png)


- instance state

- start / stop / terminate


![instance listing, conf, etc](https://user-images.githubusercontent.com/47668244/185580726-1456e5cf-9223-4645-bf54-cb9c98e7d267.png)

### Connecting

- instances

- select - connect

![get instance ssh connection command](https://user-images.githubusercontent.com/47668244/185580918-455a8a98-3e13-425f-aeee-8bc24dc2c39a.png)

- copy command paste in terminal

#### Get IP

got to EC2 instance connect - copy ip

![get instance ip](https://user-images.githubusercontent.com/47668244/185581003-1ca1a982-8b4a-4a87-b7aa-92bb39aa932c.png)

install nodejs 

migrate data

navigate to app folder

edit security group to add another rule to allow port 3000 to all

npm start

configure reverse proxy

HINT: scp to migrate data from localhost to ec2 rsync also works

create documentation of everything we have done since morning


### Migrating Files
Secure Copy (SCP) command.
`-i` identify

`-r` for when the file you're copying isn't in the same directory that your currently in

`scp -i "ssh key"" -r "your file" "destination host":"destination directory"`

for example: `scp -i eng122.pem -r C:\Users\Raphael\GitHub\week4\intro_aws\app ~/ubuntu@ec2-18-203-172-115.eu-west-1.compute.amazonaws.com:`

![app migration](https://user-images.githubusercontent.com/47668244/185581174-33a9bc31-a831-414d-b0ad-7cbe28302d4f.png)

This can be done in reverse as well, migrating files from your instance to your localhost.

#### NPM Start

![npm start](https://user-images.githubusercontent.com/47668244/185581204-4f71bd7a-faa4-4cef-9f23-b0886bd0b529.png)

Up and running...

![up   running](https://user-images.githubusercontent.com/47668244/185581394-680b4f6c-0043-4dd9-9f77-22c16f56239c.png)

working on port 3000

![port 3000](https://user-images.githubusercontent.com/47668244/185581443-0bc5f498-0c6f-46b2-a5c3-cb49649b671f.png)


## Connecting App to DB machines

Now that we've set up our app instance machine, just like in virtualisation, we want to set up a database machine.

To do this we will follow the same steps, creating an EC2 instance, with the appropriate operating system, type, volume, 


