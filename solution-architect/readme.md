AWS Regions
- A region is a cluster of data centers
- Most AWS services are region-scoped

How to choose an AWS Region?
- Compliance: some country has policy that states it's data should not leave a region without your explicit permission
- Proximity
- Available service
- Pricing

AWS Availability Zone
- It is used for providing redundancy of data in case of data corruption/failure at any one place.
- Usually it has 3 availablity zone
 
IAM (Identity and Access Management)
- Root account created by default, shouldn't be used or shared.
- Users are people within your organization, and can be grouped.
- Only users can be present in group.
- Group does not contain another group.
- AWS follows least privilege principle
- Users or Groups can be assigned JSON documents called policies

- AWS CLI
- aws configure
- IAM Roles - To provide access to AWS services on behalf of user
- Credential Report 
- Last Access (previously know as Access Advisor)

EC2
- EC2 us one of the most popular of AWS' offering
- EC2 = Elastic Compute Cloud = Infrastructure as a Service
- It mainly consists in the capability of 
    - Renting virtual Machine (EC2)
    - Storing data on virtua machines (EBS)
    - Distributing load across machines (ELB)
    - Scaling the services using an auto-scaling group (ASG)
- Knowing EC2 us fundamental to understand how the Cloud works

EC2 sizing & configuration options
- Operating System (OS): Linux, Windows or Mac OS
- How much compute power & cores (CPU)
- How much random-access memory (RAM)
- How much storage space:
    - Network-attached (EBS & EFS)
    - hardware (EC2 Instance Store)
- Network card: speed of the card, Public IP address
- Firewall rules: security group
- Bootstrap script (configure at first launch): EC2 User Data
- It is possible to bootstrap our instances using an EC2 User data script.


### Security groups
A security group is a set of firewall rules that controls the traffic to and from your instance. Inbound rules control the incoming traffic to your instance, and outbound rules control the outgoing traffic from your instance. You can assign one or more security groups to your instance. If you assign multiple security groups, all the rules are evaluated to control inbound and outbound traffic. If no value is specified the value of the source template will still be used. If the template value is not specified then the default API value will be used.

## Important Points
- If your application is not accessible (time out), then it's a security group issue
- If your appliation gives a "connection refused" error, then it's an application error or it's not launched
- All inbound traffic is blocked by default
- All outbound traffic is authorised by default


Classic Port to know
22 = SSH