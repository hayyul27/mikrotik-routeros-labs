# LAB 01-PENGENALAN ROUTER OS

## Tujuan 

Mengenal perintah dasar RouterOS: melihat informasi sistem, mengganti nama router, mengecek interface, memberi alamat IP, lalu menguji koneksi dari PC.

## Lingkungan

- Simulator : GNS3 dengan GNS3 VM sebagai server
- Router : Mikrotik CHR, RouterOS versi (isi dari hasil resource print)
- Client : 1 PC virtual (VPCS)

## Topologi

![images](topologi.png)

| Perangkat | Interface | IP Address |
|---|---|---|
| R1 | ether1 | 192.168.10.1/24 |
| PC1 | eth0 | 192.168.10.2/24 |

## Langkah

Berikut perintah yang akan kita jalankan:

1. /system resource print

![images](resource.png)

Fungsi dari perintah ini adalah untuk menampilkan versi RouterOS, RAM, dan CPU.

2. /system identity set name=R1

![images](identity.png)

Perintah ini berfungsi untuk mengganti nama Router.

3. /interface print

![images](interface.png)

Perintah ini berfungsi untuk menampilkan daftar interface. Dalam mendesain jaringan perhatikan nama dan statusnya untuk di sambungkan ke client.

4. /ip address add address=192.168.10.1/24 interface=ether1

![images](ip.png)

Perintah ini berfungsi untuk memberikan IP Address ke interface yaitu disini kita berikan ke interface 1 (ether 1).

5. /ip address print

![images](ether1.png)

Perintah ini berfungsi untuk memastikan ip address yang kita masukkan tadi sudah terpasang ke ether1.

6. /export

![images](export.png)

Perintah ini berfungsi untuk menampilkan seluruh konfigurasi yang kita lakukan tadi dalam bentuk teks. 


## Pengujian Koneksi

Kita akan sedikit lakukan simulasi dengan memberikan ip address ke PC yang terhubung ke Router. Setelah itu dari PC kita nge-ping ke ip address Router.

![images](pc.png)