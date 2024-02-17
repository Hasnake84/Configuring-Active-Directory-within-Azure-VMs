# Configuring-Active-Directory-within-Azure-VM

Create Domain Controller VM on (Windows Server 2022)

Set Domain Controller’s NIC Private IP address to be static
  
  <a href="https://imgur.com/Laebe0Z"><img src="https://i.imgur.com//Laebe0Z.png" title="source: imgur.com" /></a>

 For ping connection test with client VM set:
 
- Search > wf.msc > Inbound Rules > Protocol > ICMPv4 > ICMP Echo Request(ICMPv4-in) > Enable Rule

Create Windows 10 client VM in the same Virtual network as Domain Controller VM

# Install Active Directory

  Install Active Directory Domain Services on Domain controller VM

Start > Server Manager > Add roles and features > Roles > Select 'Active Directory Domain Services' > Install

Promote server to a Domain Controller, Setup a new forest as mydomain.com 

  <a href="https://imgur.com/hTsu0ib"><img src="https://i.imgur.com//hTsu0ib.png" title="source: imgur.com" /></a>

  <a href="https://imgur.com/oRyXvhY"><img src="https://i.imgur.com//oRyXvhY.png" title="source: imgur.com" /></a>

Restart and then log back into Domain Controller VM as user: mydomain.com\username

# Creating Organizational Unit for Admin and Employees 
 
  - Start > Windows Administrative Tools > Active Directory Users and Computers > Right click Domain name > New > Organizational Unit

<a href="https://imgur.com/aiYut1y"><img src="https://i.imgur.com//aiYut1y.png" title="source: imgur.com" /></a>

# Add a Group in the Admin Organizational Unit

  - Right click 'Admin' OU > New > Group > Name = Management > Group type = Security > Ok

<a href="https://imgur.com/HmlACWh"><img src="https://i.imgur.com//HmlACWh.png" title="source: imgur.com" /></a>

# Add a user in the Group called 'Management' in the Admin OU

  - Right click 'Management' group foler > Properties > Members > Add > Enter name > Check Names > Ok

<a href="https://imgur.com/NZUbT7Q"><img src="https://i.imgur.com//NZUbT7Q.png" title="source: imgur.com" /></a>
<a href="https://imgur.com/4kleAAK"><img src="https://i.imgur.com//4kleAAK.png" title="source: imgur.com" /></a>





