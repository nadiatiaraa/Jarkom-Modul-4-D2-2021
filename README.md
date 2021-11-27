# Jarkom-Modul-4-D2-2021

**Nama Anggota Kelompok :**
- Sabrina Lydia Simanjuntak (05111940000107)
- Zulfayanti Sofia Solichin (05111940000189)
- Nadia Tiara Febriana (05111940000217)

# VLSM
**1. Membuat Topologi**

<img width="723" alt="Screen Shot 2021-11-27 at 18 12 04" src="https://user-images.githubusercontent.com/72669398/143678815-18211e25-fb21-4e4e-a750-5948e822f6be.png">

**2. Subnetting** 

Melakukan subnetting seperti pada gambar berikut

<img width="737" alt="Screen Shot 2021-11-27 at 18 12 39" src="https://user-images.githubusercontent.com/72669398/143678833-b14ddbca-bc64-4cda-a615-3907b366821c.png">

Setelah dikelompokkan menjadi beberapa subnet, dapat dilakukan pembagian IP

<img width="492" alt="Screen Shot 2021-11-27 at 18 38 25" src="https://user-images.githubusercontent.com/72669398/143679612-33a6953c-b635-414d-9a7a-e04a70694ebe.png">

Dimana NID dan broadcast addressnya dapat dicari menggunakan tree sebagai berikut

<img width="890" alt="Screen Shot 2021-11-27 at 18 39 40" src="https://user-images.githubusercontent.com/72669398/143679922-57d1e4d6-67e5-478a-9768-0be8b3beb3ed.png">

Kemudian lakukan konfigurasi pada setiap device sesuai pembagian subnet. Contohnya pada router Foosha. Router Foosha terhubung dengan 5 device lain yaitu Cloud, Server Doriki, Client Blueno, Router Water7, Router Guanhao.

Pada interface FastEthernet0/1 yang tersambung dengan Client Blueno (Subnet A1) sehingga dimasukkan IP dan Netmask dari Subnet A1 dengan IP ditambah 0.0.0.1 sebagai berikut:

<img width="558" alt="Screen Shot 2021-11-27 at 18 39 52" src="https://user-images.githubusercontent.com/72669398/143679940-389a9744-f180-4868-a2fc-be8cbf3ab347.png">

Pada interface FastEthernet0/3/0 yang tersambung dengan Router Guanhao (Subnet A7) sehingga dimasukkan IP dan Netmask dari Subnet A7 dengan IP ditambah 0.0.0.1 sebagai berikut:
<img width="614" alt="Screen Shot 2021-11-27 at 18 40 12" src="https://user-images.githubusercontent.com/72669398/143679946-1db77dfd-7a17-4d56-a6a4-dcb3d8a64965.png">

Pada interface FastEthernet1/0 yang tersambung dengan Server Doriki (Subnet A14) sehingga dimasukkan IP dan Netmask dari Subnet A14 dengan IP ditambah 0.0.0.1 sebagai berikut:

<img width="610" alt="Screen Shot 2021-11-27 at 18 40 28" src="https://user-images.githubusercontent.com/72669398/143679948-ce9e05d3-af75-467d-b84b-cbb3a4de998d.png">

Pada interface FastEthernet1/1 yang tersambung dengan Router Water7 (Subnet A2) sehingga dimasukkan IP dan Netmask dari Subnet A2 dengan IP ditambah 0.0.0.1 sebagai berikut:

<img width="609" alt="Screen Shot 2021-11-27 at 18 40 39" src="https://user-images.githubusercontent.com/72669398/143679952-d8806618-a0bd-4b29-be6e-44215a2627c0.png">

**3. Routing** 

Melakukan konfigurasi static di tiap router agar menghasilkan seperti dibawah ini:
```
Foosha
10.22.8.0/22 via 10.22.0.2
10.22.24.0/21 via 10.22.0.2
10.22.0.128/25 via 10.22.0.2
10.22.0.4/30 via 10.22.0.2
10.22.12.0/22 via 10.22.0.10
10.22.2.0/23 via 10.22.0.10
10.22.0.16/28 via 10.22.0.10
10.22.1.0/24 via 10.22.0.10
10.22.16.0/22 via 10.22.0.10
10.22.0.36/30 via 10.22.0.10
10.22.0.12/30 via 10.22.0.10
```

```
Water7
0.0.0.0/0 via 10.22.0.1
10.22.0.128/25 via 10.22.0.6
10.22.24.0/21 via 10.22.0.6
```

```
Pucci
0.0.0.0/0 via 10.22.0.5
```
```
Guanhao
0.0.0.0/0 via 10.22.0.9
10.22.0.16/28 via 10.22.2.3
10.22.1.0/24 via 10.22.0.14
10.22.16.0/22 via 10.22.0.14
10.22.0.36/30 via 10.22.0.14
```
```
Alabasta
0.0.0.0/0 via 10.22.2.1
```
```
Oimo
0.0.0.0/0 via 10.22.0.13
10.22.16.0/22 via 10.22.1.3
```
```
Seastone
0.0.0.0/0 via 10.22.1.1
```

# CIDR
**1. Membuat Topologi**

<img width="705" alt="Screen Shot 2021-11-27 at 18 41 03" src="https://user-images.githubusercontent.com/72669398/143679954-9b059e74-a055-4f2d-8aac-15029b15f4c1.png">

**2. Subnetting** 

Melakukan labelling netmask terhadap masing-masing subnet yang tahap-tahapnya sebagai berikut :

<img width="862" alt="Screen Shot 2021-11-27 at 18 41 34" src="https://user-images.githubusercontent.com/72669398/143679955-bd4b67fd-5a1d-4e74-bc49-b9c96d90c1af.png">

<img width="890" alt="Screen Shot 2021-11-27 at 18 41 56" src="https://user-images.githubusercontent.com/72669398/143679957-62c9f048-012c-4692-92d6-d1125e9cbc13.png">

<img width="893" alt="Screen Shot 2021-11-27 at 18 42 07" src="https://user-images.githubusercontent.com/72669398/143679958-3b76c075-aceb-4c88-8282-2f8336200b0b.png">

<img width="879" alt="Screen Shot 2021-11-27 at 18 42 18" src="https://user-images.githubusercontent.com/72669398/143679978-1cf893cf-ed10-4c01-bf8b-66dd831fb7ee.png">

<img width="819" alt="Screen Shot 2021-11-27 at 18 42 30" src="https://user-images.githubusercontent.com/72669398/143679993-6fa100ad-ad6f-4a2f-9d1d-95271590fc87.png">

<img width="825" alt="Screen Shot 2021-11-27 at 18 42 39" src="https://user-images.githubusercontent.com/72669398/143679996-14506036-09ec-4df3-beb5-20069ed28a56.png">

<img width="835" alt="Screen Shot 2021-11-27 at 18 42 50" src="https://user-images.githubusercontent.com/72669398/143679997-a4228f2f-9224-45a1-8535-1ecac9a019cb.png">

<img width="835" alt="Screen Shot 2021-11-27 at 18 42 59" src="https://user-images.githubusercontent.com/72669398/143679998-6a86ac97-5523-4702-ad1a-7c9eaa5b599b.png">

Dari proses penggabungan yang telah dilakukan, didapatkan sebuah subnet besar dengan netmask  /15. Kali ini dapat menggunakan NID 192.168.0.0, netmask 255.254.0.0.

<img width="935" alt="Screen Shot 2021-11-27 at 18 43 14" src="https://user-images.githubusercontent.com/72669398/143680000-4f7119ee-9461-494a-9992-ed826bb2ac85.png">

Kemudian hitung pembagian IP dengan pohon berdasarkan penggabungan subnet yang telah dilakukan dengan menggunakan tree sebagai berikut:

<img width="532" alt="Screen Shot 2021-11-27 at 18 43 39" src="https://user-images.githubusercontent.com/72669398/143680002-c98d26e9-16b0-44c7-aae4-6dd16e1ed883.png">

**3. Routing**
**4. Testing**
