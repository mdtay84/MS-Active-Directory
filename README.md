# Microsoft Active Directory

## Objective

This lab is a setup of Active Directory (AD) on a virtual machine.  It demonstrates proficiency in understanding key concepts in the administration of AD, focusing on the management of servers, users, and groups.

### Skills Learned

- Understanding in user creation and password setup.
- Proficient in server setup for a network which includes Domain Controller, DHCP, DNS, etc.
- Knowledge of Group Policy Management (GPO) editor and how to fine tune the settings for each group.
- Development of IAM principles with creating, deleting, and locking out of users accounts as well as adding and removing users and groups objects into groups.

### Tools Used

- Oracle VMWare for a controlled environment inside a virtual machine.
- Microsoft Server 2019

## Steps
 

I installed Windows Server 2019 into a VM with VMWare and started a new domain under taylornet.com. I set up a DHCP server with a rather small scope because I have no other device to connect to.  I also am using two NIC on the Domain Controller and configured it so that access to the public internet is done through the Controller (AKA the domain controller serves as the gateway router) 

![image](MS_AD_1.png)
  

Next, I created three OUs for the three departments I will have in this company:  Finance, IT, and R & D.  I am using the GPO editor to create group policies within these departments.   As I will only have one extra device connected to this domain, I decided that modifying the user settings in the GPO policy editor would be ideal in this situation. 

![image](MS_AD_2.png)

I created some users and assigned them to one of the groups of policies specific to each department in the company.  The departments each have their own policies specific to the needs of what their roles require. 

![image](MS_AD_3.png)
 
