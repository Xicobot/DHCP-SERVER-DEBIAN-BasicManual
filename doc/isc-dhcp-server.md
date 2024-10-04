# DHCP SERVER
### Files
For the main server, we will need to edit the following files to configure it properly. First, we must install the service called `isc-dhcp-server` and configure the server with a static IP address.

First we install the service:
```
apt update 
apt upgrade
apt install isc-dhcp-server
```
After that, we can configure the following files:
`/etc/default/isc-dhcp-server`, `/etc/dhcp/dhcpd.conf` and `/etc/network/interfaces`

First, we need to configure /etc/network/interfaces to assign a static IP address.
### /etc/network/interfaces
![img](/img/address-server.png)
Change the address and the netmask to match your local network.
After that, we will configure the DHCP server files.
### 1. /etc/default/isc-dhcp-server
![img](/img/ethernet-server.png)
Change the interface to reflect your local network that will provide IP addresses.
### 2. /etc/dhcp/dhcpd.conf
![img](/img/config.png)
This is where we will assign the pool of IP addresses and other configurations. The important sections to note are the "Failover" section and the range of the IP address pool
### 3. DHCP Leases
This is an extra step, if you want to see if your DHCP gives DHCP correctly and assings a clients IP, you can check it in: `/var/lib/dhcp/dhcpd.leases`
![img](/img/LEASES-SERVER.png)
