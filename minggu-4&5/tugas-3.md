# Tugas 3 Administrasi Jaringan

## Pendapat Tentang Bagaimana Internet Bekerja

Ekosistem Internet terdiri dari beberapa bagian dan pihak yang mengatur serta mengelolanya sehingga membuat internet dapat bekerja. Pihak-pihak yang berada dalam ekosistem internet antara lain IANA, ICANN, IETF selain itu pemerintah juga turut andil dalam mengatur dan mengelola ekosistem internet. Setiap negara mendapatkan nama domain unik ccTLDs(country-code Top-Level Domains), dimana negara Tuvalu menerima PDB yang cukup tinggi karena ccTLDS nya berakhiran ".tv". Selain itu dalam ekosistem internet terdapat IP address dan Routing serta DNS (Domain Name Server), DNS mentranslasikan IP address ke Nama Server/Host. Terdapat 3 komponen DNS yaitu Namespace, NameServer, Resolvers/Clients.

## Bind9

1. Install bind9 melalu terminal dengan mengetikan perintah seperti pada gambar  

![Instal](./assets/3.png)

2. Cek dan konfigurasi file nya di /etc/bind  

![ls](./assets/4.png)

3. Buka dan konfigurasi file named.conf dan sesuaikan dengan gambar  

![named.conf](./assets/5.png)

4. Buka dan konfigurasi file named.conf.default-zones dan sesuaikan dengan gambar  

![named.conf.default-zones](./assets/6.png)
![named.conf.default-zones](./assets/7.png)

5. Buka dan konfigurasi file named.conf.options dan sesuaikan dengan gambar

![named.conf.option](./assets/8.png)
![named.conf.option](./assets/9.png)

6. Buka dan konfigurasi file named.conf.local dan sesuaikan dengan gambar

![named.conf.local](./assets/10.png)

7. Kemudian lakukan pengecekan konfigurasi dengan sudo named-checkconf. Jika tidak ada error, maka konfigurasi sudah benar.

![named-checkconf](./assets/11.png)

8. Lalu kita pindah ke folder /var/lib/bind dan konfigurasikan db.kelompok9.local seperti gambar

![db.kelompok9.local](./assets/12.png)

9. Konfigurasikan juga db.kelompok9.local.inv

![db.kelompok9.local.inv](./assets/13.png)

10. Lalu navigasikan dan konfigur file /etc/resolv.conf

![resolv.conf](./assets/15.png)

11. Jalankan perintah sudo systemctl restart named dan dig ns.kelompok9.local

![systemctl](./assets/14.png)

12. Jalankan  perintah nslookup

![nslookup](./assets/16.png)