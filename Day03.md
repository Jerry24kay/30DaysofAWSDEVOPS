![3](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/7c32ca8d-34cd-4446-8cfa-4c2197e52e91)

**Welcome to Day 3 of my 30-day AWS DevOps Challenge!**

Today, I embarked on an exciting journey of setting up an EC2 instance, installing PrestaShop, and creating an RDS database with MySQL—all seamlessly integrated to build a dynamic web application. Let's dive into the step-by-step process:



**Step 1: Launching an EC2 Instance**

I kicked off the day by launching an EC2 instance, a foundational step in the cloud environment. After configuring the instance details, security groups, and key pairs, I was ready to roll.

![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/3b22cd13-21da-4942-9335-b94312aa5d83)

For this installation i allowed inbound traffic. 
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/4fbfbd79-ace6-4e7c-8231-096846f750a2)

Now EC2 instance ready to roll!! 
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/e0d41719-ac28-46d3-b329-ff5f77e38a9a)



**Step 2: Creating an RDS Database**

Next, I delved into creating an RDS database with MySQL—a pivotal element for data storage. After setting the database instance specifications and authentication, my database was ready to power the upcoming PrestaShop installation.

![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/2202b815-00ef-430f-baee-87bd84633586)

I choose the instance i launched for this project.
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/51cd55a2-f5ff-468a-85a9-4000a62fd539)

DB ready to roll!
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/c0136919-e3fa-48db-a4b3-c93c96210a54)




**Step 3: Connecting to the Instance and Running Updates**

Using Putty and the generated key pair, I established an SSH connection to my EC2 instance. I began by running updates and installing Apache2—an essential component for web hosting.

![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/deb7cffa-556e-42f9-9d2d-bcdb3db1144c)

Installed Apache2
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/5e75181b-a93a-418f-9ec5-36e9bcbe0f8b)

Enabled the service 
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/12520ac2-3d98-4aee-bbb6-b418909028eb)



To facilitate the installation of PrestaShop, I needed PHP and specific extensions. 

![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/30c95934-647b-4fa6-8b45-f44944ea9d49)



After some setup, I downloaded PrestaShop from their GitHub repository, unzipped it, and adjusted permissions.
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/713299f0-767b-46e7-810d-ff108eb8d682)
 

![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/e0dd7e22-eb0d-4479-a33a-4d6023c3eb58)
 

permissions changed
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/8f36c247-40f8-4230-ad55-a26c843fa429)
 


**Installing PrestaShop and Overcoming Hurdles**


I encountered an initial hiccup—compatibility issues with PHP version 8. I promptly downgraded to PHP 7.4 to ensure a smooth installation process.

![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/5b5c7a2c-ff57-4bc0-99f7-4b0cb86dbc59)

 



**Navigating the PrestaShop Installation**

With PHP sorted, I initiated the PrestaShop installation. Overcoming some minor errors, I continued by addressing the installation's prerequisites, including enabling the apache mod_rewrite module for URL rewriting. This adjustment ensured a seamless installation process.

![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/0f113b95-11a4-4238-99bf-5ccb42ef82d5)

 
Error during installation
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/e83de16d-c490-4ae7-ab2b-6725638432f5)

 
This line of cmd **"sudo apt-get install php7.4-intl"** cleared the **"Intl extension is not loaded"** Error

 
I solved the Error **"Enable the Apache mod_rewrite module" **by enabling it in the conf.

 ![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/85c3a272-a29a-4ae2-8793-81d23c7aaf12)



Result after the restart of apache2
 ![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/7e5504c4-2c93-49bb-9094-7eccc4342a96)




**Integration with RDS: Testing and Success**

As the installation progressed, I seamlessly connected PrestaShop with the RDS database I had created earlier. Thorough testing ensured a successful connection and the foundation for a fully functional e-commerce platform.


Setting up the db and connecting it to my rds instance on aws
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/fff0e96a-4233-4d42-88eb-b729634793fc)
 

Tested the connection
 ![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/88974cbf-a70b-424a-a259-bc35a9d73b82)


Installation in progress. 
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/f2c941e7-0482-47ee-aa64-b2c250d4a039)

 

Installation successful
 ![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/2778581d-138a-475f-9205-941c27d6171f)



**Installation Complete: Security Measures**

With the installation successfully completed, I turned my attention to security. Deleting the installation files from the server was a crucial step to safeguard the application. I logged into the EC2 instance via SSH and removed the unnecessary files, securing the environment.

![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/1a2f3104-91b4-4aa0-bf36-4697c34d07c8)
 



**Mission Accomplished: A Functional Online Store**

And there it is—a functional PrestaShop-powered online store! What began as an EC2 instance and RDS database setup evolved into a dynamic web application ready to serve customers.

![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/044920a5-e6e3-43ca-9f63-d95c6218a8d9)

**AWS Services Utilized**: Throughout this endeavor, I made use of Amazon EC2 for hosting, Amazon RDS for database management, alongside tools like Apache2, PHP, GitHub, and Putty for seamless deployment.

As Day 3 concludes, I'm invigorated by the progress made and the wealth of knowledge gained. Tomorrow, my exploration continues as I delve into enhancing security measures and refining the performance of my cloud infrastructure. Stay curious and stay with me as we unravel the layers of AWS capabilities!








