# Configure-StaticIP-Ubuntu18Up

# Tools
1. VirtualBox v6.1
2. Ubuntu Server 18.04 dan versi terbaru

## Step 

### 1. VirtualBox

Configure Network
* Adapter 1
  [x]Enable Network Adapter

* Attached to : NAT

* Adapter 2
  [x] Enable Network Adapter

* Attached to : Host-only Adapter

* Name : VirtualBox Host-Only Ethernet Adapter
  You must set in File --> Host Network Manager --> Create --> Apply (ignore it)

### 2. In Ubuntu Server or Ubuntu Desktop
- Copy the default File configuration
- Edit the copy of File configuration
```
network:
   ethernets:
       enp0s8:
           addresses: [192.168.xx.xx/24]
           gateway4: 192.168.xx.x
           dhcp4: no
   version: 2
```
- Don't forget to save the configuration
- sudo netplan try
- sudo netplan apply


