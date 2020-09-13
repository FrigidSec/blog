    
# Active Directory Basics

### What is Active Directory(AD)
**Active Directory** is a directory service developed my Microsoft to manage  Windows domain networks. It stores information related to objects, such as Computers, Users, printers etc. Think of it as a phone book for windows.This enables a user to have one username and password and authenticate over the network using those credentials.Authentication is done using **Kerberos tickets** on Windows devices.**Active Directory** is most commonly used identity management service in the world and can be exploited without the need of exploits instead we abuse features, trusts, policies and more.


# Components of Active Directory

### Physical Active Directory Components
**Domain Controller:** A domain controller is a server that stores the Active Directory database. each domain controller has a writeable copy of the directory. It provides authentication and authorization services, Allows administrative access to manage user accounts and network resources.**Domain controller** is one of the top targets when attacking an active directory. If the domain controller is compromised the entire network is toast you could do anything you want.

**Active Directory Data Store(AD DS)**: This contains the database files and processes that store and manage directory information for users,services and applications. It is a part of the **Domain Controller**. It also contains a file named **Ntds.dit** this file contains information on active directory data and all the password hashes for the users.we can take these hashes and crack them.  This file is jackpot. It is by default stored in **%SystemRoot%\NTDS** folder on all domain controllers and is accessible only through the domain controller processes and protocols. 
 
### Logical Active Directory Components
**Active Directory Schema:** Defines every type of object that can be stored in the directory and enforces rules regarding object creation and configuration. one can think of it as a rulebook which has to be followed while creating objects and configuring them. There are  two types of object **Class Object**(Users, Computers) and **Attribute Object**(information that can be attached to an object Eg. Display Name).
 
**Domains:**  It is a logical group of users and computers that share the characteristics of centralized security and administration. Domains are used to group and manage objects in an organization. It provides an administrative boundary for applying policies to groups of objects.
 
**Trees:** A tree is a collection of Active Directory domains. All domains in the tree share a contiguous namespace. In this configuration, domains fall into a parent-child relationship, which the child domain taking on the name of the parent.
 
**Forests:** A forest is a collection of one or more Domain trees. All the trees in a forest share a common schema. In a forest all trees are connected by transitive two-way trust relationships, thus allowing users in any tree access to resources in another for which they have been given appropriate permissions and rights. By default the first domain created in a forest is called the root domain.
 
**Organizational Units(OUs):** OUs are Active Directory containers that can contain users, groups, computers and other OUs. OUs are used to represent your organization hierarchically and logically, Manage a collection of objects in a consistent way and apply policies.
