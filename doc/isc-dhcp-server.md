# DHCP SERVER
### Files
For the main server, we will need to edit the following files to configure it properly. First, we must install the service called `isc-dhcp-server` and configure the server with a static IP address.

```
apt update 
apt upgrade
apt install isc-dhcp-server
```

After that, we can configure the following files:
`/etc/default/isc-dhcp-server` and `/etc/dhcp/dhcpd.conf`

