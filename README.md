# Jarkom-Modul-5-A13-2023

## Laporan Resmi Pengerjaan Praktikum Jaringan Komputer

| No. | Anggota               | NRP          |
|-----|----------------------------|--------------|
| 1   | Rule Lulu Damara           | 5025211050   |
| 2   | Aida Fitrania Prabasati    | 5025211033	  |

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

## SOAL

### No 1

Agar topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi Aura menggunakan iptables, tetapi tidak ingin menggunakan MASQUERADE.

### Answer

Berikut adalah konfigurasi iptables pada Aura yang mencakup pengaturan agar topologi dapat mengakses keluar tanpa menggunakan MASQUERADE
```bash
ETH0_IP=$(ip -4 addr show eth0 | grep -oP '(?<=inet\s)\d+(\.\d+){3}')
iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source $ETH0_IP
```

### Description

- `ETH0_IP=$(ip -4 addr show eth0 | grep -oP '(?<=inet\s)\d+(\.\d+){3}')` untuk mengambil alamat IP dari antarmuka eth0 dan menyimpannya dalam variabel `$ETH0_IP`.
- `iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source $ETH0_IP` untuk menambahkan aturan ke tabel NAT untuk melakukan SNAT (Source NAT) pada koneksi keluar melalui antarmuka eth0. Ini memastikan bahwa paket yang keluar memiliki alamat sumber yang sesuai dengan alamat IP antarmuka `eth0`.

### Testing
Setiap route akan berhasil melakukan ping keluar, disini saya buktikan dengan melakuakn ping pada salah satu server yaitu Stark.

![Screenshot 2023-12-19 210412](https://github.com/RuleLuluDamara/Jarkom-Modul-5-A13-2023/assets/105763198/8e222bc6-7add-4eaf-af7d-56ea1b55076e)


### No 2

Kalian diminta untuk melakukan drop semua TCP dan UDP kecuali port 8080 pada TCP

### Answer
Berikut adalah syntax yang disimpan pada no2.sh GrobeForest(client) untuk melakukan drop semua TCP dan UDP kecuali port 8080 pada TCP. 
```bash
# Izinkan koneksi ke port 8080
iptables -F

iptables -A INPUT -p icmp -j ACCEPT

iptables -A INPUT -p tcp --dport 8080 -j ACCEPT

iptables -A INPUT -p tcp -j DROP

iptables -A INPUT -p udp -j DROP
```

### Description
- `iptables -A INPUT -p tcp --dport 8080 -j ACCEPT` mengizinkan koneksi ke port 8080 menggunakan protokol TCP. Ini berarti paket yang menuju ke port 8080 dengan protokol TCP akan diterima.

- `iptables -A INPUT -p tcp ! --dport 8080 -j DROP` menolak koneksi untuk semua port selain 8080 menggunakan protokol TCP. Ini berarti paket yang menuju ke port apa pun selain 8080 dengan protokol TCP akan ditolak.

- `iptables -A INPUT -p udp -j DROP` menolak semua koneksi yang menggunakan protokol UDP. Ini berarti paket dengan protokol UDP akan ditolak, tidak memperhatikan port tujuan.

### Testing
- Testing port 8080 pada TCP (berhasil)
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-5-A13-2023/assets/105763198/b527f970-8087-415d-b9d0-f6777fd7f5f1)
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-5-A13-2023/assets/105763198/264a4a9e-2496-4b7f-98e7-7ac67ea9b203)

- Testing kecuali port 8080 pada TCP (tidak berhasil)
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-5-A13-2023/assets/105763198/42440d84-9194-4ba4-b632-52631aba0f1c)
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-5-A13-2023/assets/105763198/91b68426-f58f-4a5c-9bb7-c25c8eab04af)


### No 3
Kepala Suku North Area meminta kalian untuk membatasi DHCP dan DNS Server hanya dapat dilakukan ping oleh maksimal 3 device secara bersamaan, selebihnya akan di drop.

### Answer
Berikut adalah syntax yang disimpan pada no2.sh GrobeForest(client) untuk melakukan drop semua TCP dan UDP kecuali port 8080 pada TCP. 

```bash
iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT
iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP
```

### Description
- `iptables -A INPUT -m state --state ESTABLISHED,RELATED -j ACCEPT` Menambahkan aturan ke chain INPUT untuk mengizinkan koneksi yang terkait dengan koneksi yang sudah ada (ESTABLISHED) atau terkait dengan koneksi yang masih berlangsung (RELATED).
- `iptables -A INPUT -p icmp -m connlimit --connlimit-above 3 --connlimit-mask 0 -j DROP` Menambahkan aturan ke chain INPUT untuk membatasi jumlah koneksi ICMP (ping) yang diterima. Aturan ini akan menolak paket ICMP jika jumlah koneksi dari satu alamat IP melebihi 3 secara bersamaan

### Testing
- Berikut pembuktian pada DHCP Server (Revolte)
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-5-A13-2023/assets/105763198/d606708a-ba58-4913-8849-c22e8a0832c0)

Dapat dilihat bahwa node keempat yang melakukan ping akan gagal dan tidak bisa tersambung dengan node tujuan.

### No 4
Lakukan pembatasan sehingga koneksi SSH pada Web Server hanya dapat dilakukan oleh masyarakat yang berada pada GrobeForest.

### Answer
Berikut adalah syntax pada WebServer agar koneksi SSH terbatas. 

```bash
iptables -A INPUT -p tcp --dport 22 -m iprange --src-range 192.175.8.3-192.175.11.254 -j ACCEPT
iptables -A INPUT -p tcp --dport 22 -j DROP
```

### Description

Izinkan koneksi TCP ke port 22 dari rentang alamat IP 192.175.8.3-192.175.11.254:

- `iptables -A INPUT`: Menambahkan aturan pada chain INPUT (penerimaan paket masuk).
`-p tcp`: Menentukan bahwa aturan ini hanya berlaku untuk koneksi TCP.
`--dport 22`: Spesifik untuk koneksi yang menuju ke port 22 (port standar SSH).
`-m iprange --src-range 192.175.8.3-192.175.11.254`: Menggunakan modul iprange untuk menentukan rentang alamat IP yang diizinkan (dalam hal ini, dari 192.175.8.3 hingga 192.175.11.254).
`-j ACCEPT`: Mengizinkan paket yang memenuhi kriteria di atas.

- Tolak koneksi TCP ke port 22 dari sumber yang tidak termasuk dalam rentang di atas:

`iptables -A INPUT`: Menambahkan aturan pada chain INPUT.
`-p tcp`: Menentukan bahwa aturan ini hanya berlaku untuk koneksi TCP.
`--dport 22`: Spesifik untuk koneksi yang menuju ke port 22.
`-j DROP`: Menolak paket yang memenuhi kriteria di atas.

### Testing
- Berikut pembuktian pada DHCP Server (Revolte)
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-5-A13-2023/assets/105763198/d606708a-ba58-4913-8849-c22e8a0832c0)

Dapat dilihat bahwa node keempat yang melakukan ping akan gagal dan tidak bisa tersambung dengan node tujuan.

### Nomor 5

Selain itu, akses menuju WebServer hanya diperbolehkan saat jam kerja yaitu Senin-Jumat pada pukul 08.00-16.00.

### Jawaban


### Nomor 6

Lalu, karena ternyata terdapat beberapa waktu di mana network administrator dari WebServer tidak bisa stand by, sehingga perlu ditambahkan rule bahwa akses pada hari Senin - Kamis pada jam 12.00 - 13.00 dilarang (istirahat maksi cuy) dan akses di hari Jumat pada jam 11.00 - 13.00 juga dilarang (maklum, Jumatan rek).

### Jawaban


### Nomor 7

Karena terdapat 2 WebServer, kalian diminta agar setiap client yang mengakses Sein dengan Port 80 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan dan request dari client yang mengakses Stark dengan port 443 akan didistribusikan secara bergantian pada Sein dan Stark secara berurutan.

### Jawaban


### Nomor 8

Karena berbeda koalisi politik, maka subnet dengan masyarakat yang berada pada Revolte dilarang keras mengakses WebServer hingga masa pencoblosan pemilu kepala suku 2024 berakhir. Masa pemilu (hingga pemungutan dan penghitungan suara selesai) kepala suku bersamaan dengan masa pemilu Presiden dan Wakil Presiden Indonesia 2024.

### Jawaban


### Nomor 9

Sadar akan adanya potensial saling serang antar kubu politik, maka WebServer harus dapat secara otomatis memblokir  alamat IP yang melakukan scanning port dalam jumlah banyak (maksimal 20 scan port) di dalam selang waktu 10 menit. 
(clue: test dengan nmap)

### Jawaban


### Nomor 10

Karena kepala suku ingin tau paket apa saja yang di-drop, maka di setiap node server dan router ditambahkan logging paket yang di-drop dengan standard syslog level. 

### Jawaban
