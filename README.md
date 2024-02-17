# Configuring-Active-Directory-within-Azure-VMs

Create Domain Controller VM on (Windows Server 2022)

Set Domain Controller’s NIC Private IP address to be static


 For ping connection test with client VM set:
 
- Search > wf.msc > Inbound Rules > Protocol > ICMPv4 > ICMP Echo Request(ICMPv4-in) > Enable Rule

Create Windows 10 client VM in the same Virtual network as Domain Controller VM
