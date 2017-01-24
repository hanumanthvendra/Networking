# Networking

				NETWORK BASICS


Here we are providing some idea about network and network commands

To check IP address and IP information
#ifconfig 

To set IP address
#setup

network configuration 
select ethernet
give IP address, subnet mask, gateway
close
quit
quit
#service network restart


To provide DNS information:
#vi /etc/resolv.conf
(type as follows)
nameserver (DNS IP)
ex: nameserver 202.138.103.100
save&quit


To check network connectivity:
Ping: packet internet gropher
#ping server IP

To check LAN card status:
#ping 127.0.0.1 

To check host name:
#hostname

To change host name:
#hostname (fqdn)
ex: #hostname station1.redhat.com

To assign new hostname permanently
#vi /etc/hosts 
add a new line 
<IP>	<fqdn>	<hostname>
ex:
192.168.0.1	station1.redhat.com	station1
save&quit

#vi /etc/sysconfig/network
edit as follows
hostname=<fqdn>
ex:
hostname=station1.redhat.com

To view current version of kernel 
#uname -r

To view current run level:
#runlevel

we have 6 run levels:
runlevel 0=shutdown
runlevel 1=single user mode
runlevel 2=multi user without nfs
runlevel 3=multi user with network(only text mode)
runlevel 4=un used
runlevel 5=multi user with graphics & network
runlevel 6=reboot


#netstat -ant it will gives network statistics(which port number of the server is connected to which port number of client)
#vi /etc/sysconfig/network-scripts
this is the directory stores networking information 
#ifcfg-eth0
this command gives gateway, boot protocol, netmask details
this is the file which stores IP addresses and networking details

ifdown <eth0>:
this command is used to down the device
ifup <eth0>:
this command is used to bring the interface up device
