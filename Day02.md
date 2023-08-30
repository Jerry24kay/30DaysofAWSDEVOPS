![2](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/f29bc247-1c8d-4ef5-a892-0a2bf7e18d9d)
Welcome back to my 30-day AWS DevOps journey!

On Day 2, I delved into the complex world of Virtual Private Clouds (VPCs) and delved into access control strategies. Here's a concise overview of the day's activities:



Exploring VPC Components

Day 2 revolved around a comprehensive exploration of VPC components. I examined key elements such as Elastic Load Balancers, public/private subnets, route tables, security groups, Internet gateways, and Network ACLs (NACLs). The aim was to gain hands-on experience with these foundational elements of a secure cloud infrastructure.

Integrating a Python App with the VPC Ecosystem

My objective for the day was to seamlessly integrate a Python app into the VPC environment. Using the AWS console, I created a VPC and focused on experimenting with NACLs and security groups to ensure smooth communication between the Python app and various VPC components.

Crafting a VPC Framework

Using the AWS console, I meticulously designed a VPC framework to serve as the basis for my experiments. Opting for the "VPC and more" option, I started with the default IPv4 CIDR block and selected two availability zones to further my exploration.
![vpc demo](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/3edc50a6-e1a9-45b3-b8b1-daf034bef6ce)



Overcoming VPC Association Challenges

An initial challenge arose when attempting to associate the newly created VPC with an EC2 instance. After some investigation, it became evident that a region mismatch was causing the issue. Once the regions were synchronized, the problem was resolved.



Navigating Access Control and Connectivity

My focus then shifted to access control mechanisms. Setting up an EC2 instance within a public subnet, I ensured Python3 was installed and initiated an HTTP server using python3 -m http.server 8000. However, my attempts at establishing a connection were unsuccessful.
![not reachable again](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/34cf2c4b-b4d9-48db-94b2-fcb2cf78c96e)

Recalling lessons learned on Day 1, I revisited the security group settings and added a custom inbound rule to address the issue.
![inbound rule](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/d43fdb95-54a0-47db-8fc1-eccede3ad74b)
This adjustment led to successful connections and highlighted the integral role of security groups in controlling access.
![now reachable](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/2cfb8480-1b6b-4360-91a0-f8015fba961e)




Understanding Access Control Dynamics

To further explore access control intricacies, I experimented to assess the interplay between Network ACLs (NACLs) and security groups. By fine-tuning a Network ACL inbound rule to deny custom TCP traffic on port 8000, 
![deny 8000](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/2059ccfc-ba38-4b0f-b244-7f6400d3b31e)

I observed that the rule effectively blocked connection attempts.
![not reachable again](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/23c76ec5-2fe2-4e1e-90c5-2d1e001bf398)

Additionally, a dual-test scenario involving rule orders and priorities was undertaken. Despite a "deny" rule within the NACL, access to the EC2 instance persisted due to rule number hierarchies.
![rule number](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/b672d4dd-7645-4031-bb7a-2fa1b6390bf9)

Key Insights and Future Direction

Day 2 provided a deep dive into VPC components and access control principles. A fundamental lesson emerged: the sequence and hierarchy of rules play a crucial role in defining connectivity outcomes. NACLs laid the groundwork for security groups to follow suit.

Stay curious and continue exploring, as our journey will delve further into the intricacies of public-private subnets, fortifying the security of our DevOps approach.

As we uncover the layers of AWS complexity, each revelation brings us one step closer to mastering the art of cloud operations.
