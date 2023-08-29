Welcome to the kickoff of my 30-day AWS DevOps challenge! Today marks Day 1 of this exciting journey, and I've dived headfirst into the world of AWS by setting up Jenkins on an EC2 instance. Buckle up as I recount my accomplishments, challenges, and lessons from this inaugural day.

Starting Strong: EC2 Instance and SSH
My day began by launching an Ubuntu EC2 instance on AWS's free tier. Utilizing Putty as my preferred SSH client, I swiftly connected to the instance using the key pair I had created. Within moments, I found myself immersed in the Ubuntu environment, ready to take on the day's challenges.

Laying the Groundwork: Updates and Java 11
With the instance up and running, my first order of business was ensuring its stability. I executed both an update and an upgrade to the system, guaranteeing that I was working with the latest packages. Next, I installed Java 11 to provide a robust runtime environment for the tools and technologies that would follow.

The Main Event: Installing Jenkins
The highlight of the day was undoubtedly installing Jenkins, a pivotal step in establishing a DevOps pipeline. Following the guidance of the Jenkins documentation, I obtained the repository information required for the installation. Armed with a curl command, I seamlessly installed Jenkins on the EC2 instance, setting the stage for further exploration.

A Hurdle Overcome: Opening the Port
As I excitedly attempted to access Jenkins via my browser using the instance's public IP, I encountered a minor roadblock. The connection failed to be established. A quick diagnosis revealed that I had overlooked configuring the security group's inbound rule for port 8080, the default port for Jenkins. Without delay, I added a rule to allow TCP traffic on port 8080 from all sources. A refreshed browser, and there it was "the Jenkins interface gleaming on my screen".

Conclusion: Day 1 Triumphs
And so, on this eventful Day 1 of my 30-day AWS DevOps challenge, I conquered several milestones. From setting up an Ubuntu EC2 instance and navigating SSH to successfully installing Jenkins and tackling connectivity issues, I've gained invaluable insights into the world of cloud computing, automation, and persistence.

Throughout the day, I utilized a suite of powerful tools and technologies, including AWS's EC2 for virtualized computing resources, Ubuntu as the operating system, Putty for SSH access, and Jenkins for automation and CI/CD. Notably, I worked within the default Virtual Private Cloud (VPC) settings, which streamlined my setup process and allowed me to focus on the task at hand.

With the curtain drawn on this first day, I'm excited to continue my journey. Tomorrow promises more exploration of VPC, security groups, and Network ACLs (NACLs) as I delve into the foundations of network security within AWS. These elements are crucial in establishing a robust and secure environment for my DevOps practices.

Join me as I navigate the path to DevOps excellence in the coming days, unravelling the intricacies of AWS services and weaving them into the fabric of my projects.
