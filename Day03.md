![3](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/7c32ca8d-34cd-4446-8cfa-4c2197e52e91)


Today i will be working on setting up an ec2 instance, then install prestastore on it. Create an rds with mysql and link the db with the instance. 


Step 1: Launch an EC2 Instance
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/3b22cd13-21da-4942-9335-b94312aa5d83)

For this installation i will allow inbound traffic. 
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/4fbfbd79-ace6-4e7c-8231-096846f750a2)

Now EC2 instance is succesfully launched. 
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/e0d41719-ac28-46d3-b329-ff5f77e38a9a)



Step 2.Creating RDS Database
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/2202b815-00ef-430f-baee-87bd84633586)

Setting up the EC2 connection. Rembember the EC2 instance we just lanuched. Yeah i will choose the ec2 for this database.
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/51cd55a2-f5ff-468a-85a9-4000a62fd539)

DB Created successfully
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/c0136919-e3fa-48db-a4b3-c93c96210a54)





Step 3. Connect to the instance and run updates.  
I will be using Putty and the key pair I generated.
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/deb7cffa-556e-42f9-9d2d-bcdb3db1144c)

Next is to install apache2. We need a server
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/5e75181b-a93a-418f-9ec5-36e9bcbe0f8b)

Enabling apache2 and starting the service. 
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/12520ac2-3d98-4aee-bbb6-b418909028eb)

Now I need to install php and the required extensions for prestashop. 
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/30c95934-647b-4fa6-8b45-f44944ea9d49)

Next step is to wget the prestashop from their github repo
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/713299f0-767b-46e7-810d-ff108eb8d682)
 

Then unzip it
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/e0dd7e22-eb0d-4479-a33a-4d6023c3eb58)
 

Next is to change the permissions 
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/8f36c247-40f8-4230-ad55-a26c843fa429)
 


Encountered some error during the installation, i had to downgrade the php version from v8 to v7.4
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/5b5c7a2c-ff57-4bc0-99f7-4b0cb86dbc59)

 



Step 5. Now i can begin the installation of prestastore 

![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/0f113b95-11a4-4238-99bf-5ccb42ef82d5)

 

Another error
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/e83de16d-c490-4ae7-ab2b-6725638432f5)

 
This line of cmd cleared the first error

sudo apt-get install php7.4-intl
 
For the second error I had to enable the apache mod_rewrite module for url rewriting and enable it in the conf as well.
 ![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/85c3a272-a29a-4ae2-8793-81d23c7aaf12)



Result after the restart of apache2
 ![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/7e5504c4-2c93-49bb-9094-7eccc4342a96)



Now i can continue the installation. 

Setting up the db and connecting it to my rds instance on aws
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/fff0e96a-4233-4d42-88eb-b729634793fc)
 

Testing the connection
 ![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/88974cbf-a70b-424a-a259-bc35a9d73b82)



Installation in progress. 
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/f2c941e7-0482-47ee-aa64-b2c250d4a039)

 

Installation successful
 ![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/2778581d-138a-475f-9205-941c27d6171f)


Now i need to delete the install file from the server for security reasons. 
So i logged into the ec2 instance using ssh 
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/1a2f3104-91b4-4aa0-bf36-4697c34d07c8)
 

Finally we have our store. 
![image](https://github.com/Jerry24kay/30DaysofAWSDEVOPS/assets/54981872/044920a5-e6e3-43ca-9f63-d95c6218a8d9)



