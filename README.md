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

- instance state

- start / stop / terminate

### Connecting

- instances

- select - connect

- copy command paste in terminal


#### Get IP

got to EC2 instance connect - copy ip






install nodejs 

migrate data

navigate to app folder

edit security group to add another rule to allow port 3000 to all

npm start

configure reverse proxy

HINT: scp to migrate data from localhost to ec2 rsync also works

create documentation of everything we have done since morning


### SCP
Secure Copy (SCP)
`-i` identify

`-r` for when the file you're copying isn't in the same directory that your currently in

`scp -i "ssh key"" -r "your file" "destination host":`