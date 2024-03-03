# This is the network config written by 'subiquity'
network:
  ethernets:
     enp2s0:
       dhcp4: true
       optional: true
     enp3s0:
       dhcp4: false
       optional: true
       addresses: [192.168.100.2/24]
       optional: true
       nameservers:
        addresses: [255.255.255.0]
  version: 2

