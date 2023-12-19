# Jarkom-Modul-5-A13-2023

## Laporan Resmi Pengerjaan Praktikum Jaringan Komputer

| No. | Anggota               | NRP          |
|-----|----------------------------|--------------|
| 1   | Rule Lulu Damara           | 5025211050   |

## Topologi
Berikut merupakan topologi yang digunakan:
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-5-A13-2023/assets/105763198/96402671-6bf0-4dcb-a000-4c8bbe81e049)

## Pembagian Subnet
Berikut merupakan Pembagian subnet yang digunakan:
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-5-A13-2023/assets/105763198/2e8525ff-eeab-40c0-99d7-dc39c9b5e876)

## Prefix IP
Prefix IP yang digunakan adalah ```bash 192.175.x.x```

## Tree
Berikut merupakan tree yang digunakan:
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-5-A13-2023/assets/105763198/317f64f5-3527-4b07-b2d8-f7e02d6ed9db)


## Pembagian IP 
Berikut merupakan Ppemabgian IP yang digunakan:
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-5-A13-2023/assets/105763198/48e4bb56-085d-491d-b3d4-bee39e6f460e)

## Konfigurasi Node
AURA
```bash
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 192.175.14.145
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.175.14.149
	netmask 255.255.255.252

up echo nameserver 192.168.122.1 > /etc/resolv.conf

route add -net 192.175.0.0 netmask 255.255.248.0 gw 192.175.14.150
route add -net 192.175.8.0 netmask 255.255.252.0 gw 192.175.14.150
route add -net 192.175.14.140 netmask 255.255.255.252 gw 192.175.14.146
route add -net 192.175.14.136 netmask 255.255.255.252 gw 192.175.14.146
route add -net 192.175.12.0 netmask 255.255.254.0 gw 192.175.14.146
route add -net 192.175.14.0 netmask 255.255.255.128 gw 192.175.14.146
route add -net 192.175.14.132 netmask 255.255.255.252 gw 192.175.14.146
route add -net 192.175.14.128 netmask 255.255.255.252 gw 192.175.14.146
```

FRIEREN
```bash
auto eth0
iface eth0 inet static
	address 192.175.14.146
	netmask 255.255.255.252
	gateway 192.175.14.145

auto eth1
iface eth1 inet static
	address 192.175.14.137
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.175.14.141
	netmask 255.255.255.252

up echo nameserver 192.168.122.1 > /etc/resolv.conf

route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.175.14.145
route add -net 192.175.12.0 netmask 255.255.254.0 gw 192.175.14.138
route add -net 192.175.14.0 netmask 255.255.255.128 gw 192.175.14.138
route add -net 192.175.14.132 netmask 255.255.255.252 gw 192.175.14.138
route add -net 192.175.14.128 netmask 255.255.255.252 gw 192.175.14.138
```

HIMMEL
```bash
auto eth0
iface eth0 inet static
	address 192.175.14.138
	netmask 255.255.255.252
	gateway 192.175.14.137

auto eth1
iface eth1 inet static
	address 192.175.14.1
	netmask 255.255.255.128

auto eth2
iface eth2 inet static
	address 192.175.12.1
	netmask 255.255.254.0

up echo nameserver 192.168.122.1 > /etc/resolv.conf

route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.175.14.137 
route add -net 192.175.14.132 netmask 255.255.255.252 gw 192.175.14.3
route add -net 192.175.14.128 netmask 255.255.255.252 gw 192.175.14.3
```

FERN
```bash
auto eth0
iface eth0 inet static
	address 192.175.14.3
	netmask 255.255.255.128
	gateway 192.175.14.1

auto eth1
iface eth1 inet static
	address 192.175.14.133
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.175.14.129
	netmask 255.255.255.252

up echo nameserver 192.168.122.1 > /etc/resolv.conf

route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.175.14.1
```

HEITER
```bash
uto eth0
iface eth0 inet static
	address 192.175.14.150
	netmask 255.255.255.252
	gateway 192.175.14.149

auto eth1
iface eth1 inet static
	address 192.175.8.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 192.175.0.1
	netmask 255.255.248.0

up echo nameserver 192.168.122.1 > /etc/resolv.conf

route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.175.14.149
```

## Web Server
SEIN
```bash
auto eth0
iface eth0 inet static
	address 192.175.8.2
	netmask 255.255.255.0
	gateway 192.175.8.1

up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

STARK
```bash
auto eth0
iface eth0 inet static
	address 192.175.14.142
	netmask 255.255.255.252
	gateway 192.175.14.141
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

## DHCP
RITCHER
```bash
auto eth0
iface eth0 inet static
	address 192.175.14.134
	netmask 255.255.255.252
	gateway 192.175.14.133
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

REVOLTE (DHCP SERVER)
```bash
auto eth0
iface eth0 inet static
	address 192.175.14.130
	netmask 255.255.255.252
	gateway 192.175.14.129
 up echo nameserver 192.168.122.1 > /etc/resolv.conf

```

## CLIENT
TURK REGION
```bash
#auto eth0
#iface eth0 inet static
#	address 192.175.0.2
#	netmask 255.255.248.0
#	gateway 192.175.0.1

auto eth0
iface eth0 inet dhcp
gateway 192.175.0.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

GROBEFOREST
```bash
#auto eth0
#iface eth0 inet static
#	address 192.175.8.3
#	netmask 255.255.255.0
#	gateway 192.175.8.1

auto eth0
iface eth0 inet dhcp
gateway 192.175.8.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

LAUBHILLS
```bash
#auto eth0
#iface eth0 inet static
#	address 192.175.12.2
#	netmask 255.255.254.0
#	gateway 192.175.12.1

auto eth0
iface eth0 inet dhcp
gateway 192.175.12.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

SCHWERMOUNTAIN
```bash
#auto eth0
#iface eth0 inet static
#	address 192.175.14.2
#	netmask 255.255.255.128
#      gateway 192.175.14.1

auto eth0
iface eth0 inet dhcp
gateway 192.175.14.1
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

## Konfigurasi DHCP pada REVOLTE (dhcpd.conf)

```bash
apt update
apt install isc-dhcp-server -y
echo 'INTERFACESv4="eth0"'> /etc/default/isc-dhcp-server

echo ' 
#a1
subnet 192.175.14.128 netmask 255.255.255.252 { 
}

#a2
subnet 192.175.14.132 netmask 255.255.255.252 { 
}

#a5
subnet 192.175.14.136 netmask 255.255.255.252 { 
}

#a6
subnet 192.175.14.140 netmask 255.255.255.252 { 
}

#a7
subnet 192.175.14.144 netmask 255.255.255.252 { 
}

#a8
subnet 192.175.14.148 netmask 255.255.255.252 { 
}

#schewermountain a3
subnet 192.175.14.0 netmask 255.255.255.128 { 
    range 192.175.14.4 192.175.14.126;
    option routers 192.175.14.1;
    option broadcast-address 192.175.14.127;
    option domain-name-servers 192.175.14.134;
    default-lease-time 180;
    max-lease-time 5760;
}

#laubhills a4
subnet 192.175.12.0 netmask 255.255.254.0 { 
    range 192.175.12.4 192.175.13.254;
    option routers 192.175.12.1;
    option broadcast-address 192.175.13.255;
    option domain-name-servers 192.175.14.134;
    default-lease-time 180;
    max-lease-time 5760;
}

#turkregion a9
subnet 192.175.0.0 netmask 255.255.248.0 { 
    range 192.175.0.2 192.175.7.254;
    option routers 192.175.0.1;
    option broadcast-address 192.175.7.255;
    option domain-name-servers 192.175.14.134;
    default-lease-time 180;
    max-lease-time 5760;
}

#grobeforest a10
subnet 192.175.8.0 netmask 255.255.252.0 { 
    range 192.175.8.3 192.175.11.254;
    option routers 192.175.8.1;
    option broadcast-address 192.175.11.255;
    option domain-name-servers 192.175.14.134;
    default-lease-time 180;
    max-lease-time 5760;
}'> /etc/dhcp/dhcpd.conf
service isc-dhcp-server start
```

## Konfigurasi DHCP Relay pada HIMMEL DAN HEITER (dhcpd.conf)

```bash
apt-get update
apt-get install isc-dhcp-relay -y
service isc-dhcp-relay start

echo ' 
SERVERS="192.175.14.130"

INTERFACES="eth0 eth1 eth2"

OPTIONS=""
'> /etc/default/isc-dhcp-relay
```
