# Jarkom-Modul-2-2024-IT41.

Anggota Kelompok

|Nama|NRP|
|----|---|
| Wira Samudra Siregar | 5027231041 |
| Adi Satria Pangestu | 5027231043 |

**Topologi**

![image](https://github.com/user-attachments/assets/be20349e-5fe9-4ed4-ab57-f3dab68e4ee3)

**Prefix **
|Kelompok|Prefix IP|
|----|---|
| IT41 | 192.237 |
### (Konfigurasi)
Nusantara
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 192.237.1.1
	netmask 255.255.255.0

auto eth2
iface eth2 inet static
	address 192.237.2.1
	netmask 255.255.255.0
```

Sriwijaya
```
auto eth0
iface eth0 inet static
	address 192.237.1.2
	netmask 255.255.255.0
	gateway 192.237.1.1
```

Sanjaya
```
auto eth0
iface eth0 inet static
	address 192.237.1.3
	netmask 255.255.255.0
	gateway 192.237.1.1
```

Solok
```
auto eth0
iface eth0 inet static
	address 192.237.1.4
	netmask 255.255.255.0
	gateway 192.237.1.1
```

Samaratungga
```
auto eth0
iface eth0 inet static
	address 192.237.1.5
	netmask 255.255.255.0
	gateway 192.237.1.1
```

Ken Arok
```
auto eth0
iface eth0 inet static
	address 192.237.1.6
	netmask 255.255.255.0
	gateway 192.237.1.1
```

Majapahit
```
auto eth0
iface eth0 inet static
	address 192.237.2.2
	netmask 255.255.255.0
	gateway 192.237.2.1
```

Kotalingga
```
auto eth0
iface eth0 inet static
	address 192.237.2.3
	netmask 255.255.255.0
	gateway 192.237.2.1
```

Tanjungkulai
```
auto eth0
iface eth0 inet static
	address 192.237.2.4
	netmask 255.255.255.0
	gateway 192.237.2.1
```

Bedahulu
```
auto eth0
iface eth0 inet static
	address 192.237.2.5
	netmask 255.255.255.0
	gateway 192.237.2.1
```

Setup Nusantara (router)
```
iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.237.0.0/16
echo nameserver 192.168.122.1 > /etc/resolv.conf
```

Setup Node lain
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Soal 1
Untuk mempersiapkan peperangan World War MMXXIV (Iya sebanyak itu), Sriwijaya membuat dua kotanya menjadi web server yaitu Tanjungkulai, dan Bedahulu, serta Sriwijaya sendiri akan menjadi DNS Master. Kemudian karena merasa terdesak, Majapahit memberikan bantuan dan menjadikan kerajaannya (Majapahit) menjadi DNS Slave. 

### Soal 2
Karena para pasukan membutuhkan koordinasi untuk melancarkan serangannya, maka buatlah sebuah domain yang mengarah ke Solok dengan alamat sudarsana.xxxx.com dengan alias www.sudarsana.xxxx.com, dimana xxxx merupakan kode kelompok. Contoh: sudarsana.it01.com.

### Soal 3
Para pasukan juga perlu mengetahui mana titik yang akan diserang, sehingga dibutuhkan domain lain yaitu pasopati.xxxx.com dengan alias www.pasopati.xxxx.com yang mengarah ke Kotalingga.

### Soal 4
Markas pusat meminta dibuatnya domain khusus untuk menaruh informasi persenjataan dan suplai yang tersebar. Informasi dan suplai meme terbaru tersebut mengarah ke Tanjungkulai dan domain yang ingin digunakan adalah rujapala.xxxx.com dengan alias www.rujapala.xxxx.com.

### Soal 5
Pastikan domain-domain tersebut dapat diakses oleh seluruh komputer (client) yang berada di Nusantara.
