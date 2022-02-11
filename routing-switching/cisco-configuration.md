# Cisco Configuration

**Router add IP Address**
<<<<<<< HEAD
    
    router>en
    router#conf
    config#int fa0/0
    config-if#ip add [ipaddress] [netmask]
    config-if#no sh
=======
> router>en
> router#conf
> config#int fa0/0
> config-if#ip add [ipaddress] [netmask]
> config-if#no sh
>>>>>>> f6a16b68114343a4ab57f57c63cc6f68d207e6f8


**Route Command [static]**
    
    router>en
    router#conf
    config#ip route [ipaddress:netID] [netmask] [interface gateway]


**Route command [dynamic] (RIP)**

    router>en
    router#conf
    config#router rip
    config-router#ver 1 or ver 2
    config-router#network network address


**Route command [dynamic] (EIGRP)**

    router>en
    router#conf
    config#router eigrp [id (example.100)]
    config-router#network [direct network] [wildcart mask]
    config-router#exit


**Route command [dynamic] (OSPF)**

    router>en
    router#conf
    config#router ospf [id (example.20)]
    config-router#network [direct network] [wildcart mask] [area (example 0)]
    config-router#exit


**Vlan add**

    switch>en
    switch#conf
    config#vlan [id (example 2)]
    config-vlan>NAME [segment (example KEUANGAN)]
    switch#show vlan (view the vlan config)


**Vlan add member by port**

    switch>en
    switch#conf
    config#int port (example fa0/1)
    config-if#sw mo acc
    config-if#sw acc vlan [id (example 2)]
    config-if#exit


**Vlan add member by port [trunk]**
    
    switch>en
    switch#conf
    config#int port (example fa0/1)
    config-if#sw mo trunk


**Switch add Name**
    
    switch>en
    switch#conf
    config#hostname [Name (example SWITCH_VTPSERVER)]

 

**Switch add password**

    switch>en
    switch#conf
    config#line console 0
    config-line#password [password (example CISCO)]
    config-line#login
    config-line#exit


**InterVlan Routing**

    router>en
    config#int [sub interface (example fa0/1.1)]
    config-subif#encapsulation dot1Q 2
    config-subif# ip add [gateway vlan] [netmask] (example 192.168.100.1 255.255.255.0)


**DHCP (router)**

    router>en
    config#ip dhcp excluded [ip start] [ip end]
    config#ip dhcp pool [pool name]
    dhcp-config#default-router [default gateway]
    dhcp-config#dns-server [IP DNS]
    dhcp-config#network [default gateway] [netmask]
    dhcp-config#end

