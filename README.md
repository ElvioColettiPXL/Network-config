# Network-config
Natuurlijk! Hier is wat je in je GitHub repository moet zetten:

### 1. Router Configuratie (router-config.txt)
```plaintext
hostname Router
!
interface GigabitEthernet0/0/0
 ip address 192.168.1.1 255.255.255.0
 ipv6 address 2001:db8:1::1/64
!
interface GigabitEthernet0/0/1
 ip address 192.168.2.1 255.255.255.0
 ipv6 address 2001:db8:2::1/64
!
ip route 0.0.0.0 0.0.0.0 192.168.1.1
ipv6 route ::/0 2001:db8:1::1
!
line vty 0 4
 transport input ssh
 login local
!
username admin privilege 15 secret cisco123
!
enable secret cisco123
!
```

### 2. Switch Configuratie (switch-config.txt)
```plaintext
hostname Switch1
!
interface Vlan1
 ip address 192.168.1.2 255.255.255.0
 ipv6 address 2001:db8:1::2/64
!
line vty 0 4
 transport input ssh
 login local
!
username admin privilege 15 secret cisco123
!
enable secret cisco123
!


