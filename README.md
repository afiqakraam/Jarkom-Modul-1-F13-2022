# Jarkom-Modul-1-F13-2022
Nama Anggota | NRP
------------------- | --------------
Hesekiel Nainggolan | 5025201054
Khuria Khusna | 5025201053
Afiq Akram | 5025201270

## Nomer 1
Sebutkan web server yang digunakan pada `monta.if.its.ac.id`! 

### Solusi
Gunakan filter :

```
http.host == “monta.if.its.ac.id”
```

Maka akan muncul paket yang mengandung host `monta.if.its.ac.id`

![image.png](img/soal1a.png)

Kemudian kami menggunakan `FOLLOW – TCP STREAM` untuk menampilkan webserver yang digunakan:

<img src="img/soal1b.png">


Jadi webserver yang digunakan adalah **nginx/1.10.3** 


## Nomer 2
Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website `monta.if.its.ac.id` , judul TA apa yang dibuka oleh ishaq ?

### Solusi
pertama kita mencari lokasi dari judul TA dengan menggunakan `frame contains "detailTopik"` 

<img src="img/soal2a.png">

setelah kita mengetahui lokasi dari topik untuk TA, maka selanjutnya kita `extrak object-http`

<img src="img/soal2b.png">

kemudian kita download file lihatTopik, dan kemudian kita akan melihat judul TA yang tersedia:
```
Deteksi Sentimen pada Data Audio
Prediksi produk belanjaan
Cloud Provisioning dengan menggunakan OBL dan FSO
Cloud Provisioning dengan menggunakan OBL dan SSA
Cloud Provisioning dengan menggunakan GA-ANN
```

## Setelah Revisi

## Nomor 2
Pertama kita `export HTTP`, setelah itu kita dowbload file, kecuali yang bentuk gif. 

<img src="img/soal2b.png">

Kemudian kita save file tersebut dalam bentuk .html agar lebih mudah dalam pencarian judul TA
Akhrinya kita akan menemukan judul TA yang dibuka pada file `194.html`

<img src="img/k.PNG">

Maka akan terlihat bahwa topik TA yang dilihat adalah `Evaluasi unjuk kerja User Space Filesystem (FUSE)
oleh WAHYU SUADI, Rabu 17 Maret 2021 pukul 05:13:50 WIB`

## Nomor 3

Filter sehingga wireshark hanya menampilkan paket yang menuju port 80! 

### Solusi
untuk memfilter semua paket yang menuju port 80 maka menggunakan `display filter tcp.dstport == 80 || udp.dstport == 80`. Penggunaan `dst` dikarenakan paket yang `menuju`, maka digunakan `dst`.
Maka akan menampilkan paket - paket yang menuju `port 80`

<img src="img/soal3a.png">

## Nomor 4

Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!

### Solusi
untuk memfilter semua paket yang berasal dari port 21 maka menggunakan `display filter tcp.srcport == 21 || udp.srcport == 21`. Penggunaan `src` dikarenakan paket yang `berasal`, maka digunakan `src`.
Maka akan menampilkan paket - paket yang menuju `port 21`

<img src="img/soal4a.png">

## Nomor 5

Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!

### Solusi
untuk memfilter semua paket yang berasal dari port 443 maka menggunakan `display filter tcp.srcport == 443 || udp.srcport == 443`. 
Maka akan menampilkan paket - paket yang menuju `port 443`

<img src="img/soal5.PNG">

## Nomor 6
Filter sehingga wireshark hanya menampilkan paket yang menuju ke `lipi.go.id`!

### Solusi
untuk memfilter semua paket yang menuju `lipi.go.id` kita menggunakan `http.host` dikarenakan alamat yang dituju berupa sebuah link, maka menggunakan `http.host`

<img src="img/soal6.png">

## Nomor 7
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

### Solusi
untuk menemukan ip, maka dicari dahulu menggunakan `cmd IPconfig`, maka akan didapat ip address milik kita. kemudian buka wireshark, kemudian ketik `ip.src` pada display filter dengan alamat yang dituju merupakan alamat ip yang sudah didapat.

<img src="img/soal7.png">

## Nomor 8


