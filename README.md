# AWS Security Group, NACL, Internet Gateway, Public Subnet, and EC2 Configuration
Overview: This project involved configuring a secure AWS environment using Security Groups, Network ACLs (NACLs), an Internet Gateway, a Public Subnet, and EC2 instances. The goal was to establish a secure, accessible, and scalable infrastructure.

*Components*
- Internet Gateway:
An Internet Gateway was attached to the VPC to allow the instances within the public subnet to communicate with the internet. This setup is essential for public-facing applications or any scenario requiring internet access.

- Public Subnet:
A public subnet was created within the VPC, allowing the deployment of EC2 instances that require direct access to the internet. The subnet was associated with a route table that directed internet-bound traffic through the Internet Gateway.

- EC2 Instances: EC2 instances were launched within the public subnet. These instances were configured to be accessible over the internet, with Security Groups controlling the specific types of traffic (e.g., SSH, HTTP/HTTPS) allowed.

- Security Groups: Security Groups were configured to permit only necessary traffic to the EC2 instances. For instance, SSH access was limited to specific IP addresses, and web traffic was allowed on ports 80 and 443. This provided a stateful firewall at the instance level.

- Network ACLs: NACLs were set up at the subnet level to further control inbound and outbound traffic. These rules provided an additional stateless firewall mechanism, offering an extra layer of security by defining both allow and deny rules for traffic entering or leaving the public subnet.

*This project involved configuring AWS Security Groups (SGs) and Network Access Control Lists (NACLs) to enhance the security of an AWS infrastructure using EC2.* 
![Archtecture_Digrame]()
