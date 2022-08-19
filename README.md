# Cloud Computing with AWS

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

![EC2 instance on AWS](https://user-images.githubusercontent.com/47668244/185410403-d6784a4f-d98e-4bf4-ba29-39958cb70077.png)

EC2 (elastic comput service) the machine we'd like to build based on our requirements to deploy on the cloud.

--> personal use - official use - gaming

### Conventions & Practices

- AWS naming convention for services - `group_person_task` - for example - `eng122_Shahrukh_ec2`

- When not in use (09:00 - 18:00) terminate. It costs money to run. Ask if you want to run out of hours, so that it can be authorised.

- for the duration of this course ensure you are logged in in Ireland - `Europe (Ireland) eu-west-1`.

- Do not delete anyone else's services

- DO NOT share AWS account details or keys with anyone - so don't push them to github!!!

#### Security groups

when administrating security groups, you should name your security group relevant to it's role and your instance machine.

## Set Up

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



