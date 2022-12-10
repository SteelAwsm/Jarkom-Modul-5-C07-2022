# Jarkom-Modul-5-C07-2022

laporan resmi Praktikum Jaringan Komputer Modul 5 tahun 2022

Anggota Kelompok C07 :
* 5025201274 - Alif Adrian Anzary
* 5025201122 - Marsyavero Charisyah Putra
* 5025201209 - Hemakesha Ramadhani Heriqbaldi

## Metode Perhitungan

Metode Perhitungan yang digunakan adalah VLSM, tree disusun dengan node yang memiliki host terbesar berada di paling atas (A1), sampai terkecil (A7, A8)

## Subnet Tree
![image](https://user-images.githubusercontent.com/78362238/206858839-f621b085-d62d-4a48-b053-705ac7911c76.png)

## Pembagian Subnet
![image](https://user-images.githubusercontent.com/78362238/206858863-df2db5d2-01fd-4cb6-b65e-01ee9d7e48d3.png)


## Konfigurasi Network Node

- ### Strix
```
#Nat
auto eth0
iface eth0 inet static
address 192.168.122.213
netmask 255.255.255.0
gateway 192.168.122.1

#A7
auto eth1
iface eth1 inet static
	address 10.13.0.1
	netmask 255.255.255.252

#A8
auto eth2
iface eth2 inet static
	address 10.13.0.5
	netmask 255.255.255.252
```

- ### Westalis
```
#A8
auto eth0
iface eth0 inet static
	address 10.13.0.6
	netmask 255.255.255.252
        gateway 10.13.0.5

#A1
auto eth1
iface eth1 inet static
	address 10.13.4.1
	netmask 255.255.252.0

#A4
auto eth2
iface eth2 inet static
	address 10.13.0.65
	netmask 255.255.255.128

#A6
auto eth3
iface eth3 inet static
	address 10.13.0.25
	netmask 255.255.255.248
```

- ### Ostania
```
#A7
auto eth0
iface eth0 inet static
	address 10.13.0.2
	netmask 255.255.255.252
        gateway 10.13.0.1

#A2
auto eth1
iface eth1 inet static
	address 10.13.2.1
	netmask 255.255.254.0

#A5
auto eth3
iface eth3 inet static
	address 10.13.0.17
	netmask 255.255.255.248

#A3
auto eth2
iface eth2 inet static
	address 10.13.1.1
	netmask 255.255.255.0
```

- ### Eden
```
#A6
auto eth0
iface eth0 inet static
	address 10.13.0.26
	netmask 255.255.255.248
    gateway 10.13.0.5
```

- ### Wise
```
#A6
auto eth0
iface eth0 inet static
	address 10.13.0.27
	netmask 255.255.255.248
    gateway 10.13.0.5
```

- ### Garden
```
#A3
auto eth0
iface eth0 inet static
	address 10.13.0.18
	netmask 255.255.255.248
    gateway 10.13.0.1
```

- ### SSS
```
#A3
auto eth0
iface eth0 inet static
	address 10.13.0.19
	netmask 255.255.255.248
    gateway 10.13.0.1
```

- ### (Client) Forger, Desmond, Blackbell, Briar
```
auto eth0
iface eth0 inet dhcp
```