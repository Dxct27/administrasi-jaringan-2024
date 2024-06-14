

`Tugas ini merupakan tugas mata kuliah Konsep Jaringan yang dibimbing oleh Bpk. Dr. Ferry Astika Saputra,ST, M.Sc`

## Table of Contents
- [Installing NTP Client](#installing-ntp-client)
- [Install Apache-FM](#install-apache-fm)
- [Install PHP 8.2](#install-php-82)
- [Install PHP-FM](#install-php-fm)
- [Install MariaDB](#install-mariadb)
- [Email System](#email-system)
- [Install Dovecot Server](#install-dovecot-server)
  - [Last Check](#last-check)





# Installing NTP Client

Lakukan instalasi paket layanan sinkronisasi waktu

![](assets/1.png)

Pastikan konfigurasi timezone ke Asia/Jakarta

![](assets/2.png)

Melakukan konfigurasi Real Time Clock (RTC) untuk merefer ke UTC (Coordinated Universal Time)


![](assets/3.png)

Mengaktifkan NTP Client untuk sinkronisasi waktu

![](assets/4.png)

Menyunting file timesyncd.conf untuk mengarah ke NTP server terdekat untuk mendapatkan waktu 
delay terpendek. Biasanya setiap organisasi atau negara mempunyai NTP Server sendiri

![](assets/6.png)

![](assets/5.png)

Restart layanan sinkronisasi waktu dan pastikan layanan berjalan dengan benar

![](assets/7.png)


# Install Apache-FM

Installing Apache2

![](assets/8.png)

Konfigurasi Apache2

`nano /etc/apache2/conf-enabled/security.conf`

`line 12 : change`

`ServerTokens Prod`

![](assets/9.png)

![](assets/10.png)

<br>

`nano vi /etc/apache2/mods-enabled/dir.conf`

`add file name that it can access only with directory's name`

`DirectoryIndex index.html index.htm`

![](assets/11.png)

![](assets/12.png)

<br>

`nano /etc/apache2/apache2.conf`

`line 70 : add to specify server name`

`ServerName www.kelompok9.local`

![](assets/13.png)

![](assets/14.png)

<br>

`nano /etc/apache2/sites-enabled/000-default.conf`

`line 11 : change to webmaster's email`

`ServerAdmin webmaster@kelompok9.local`

`systemctl reload apache2`

![](assets/15.png)

![](assets/16.png)

![](assets/17.png)


Test ke web browser




# Install PHP 8.2







<!-- ![](assets/phpinfo.png) -->

# Install PHP-FM





<!-- ![](assets/18.png) -->


# Install MariaDB





# Email System

![](assets/19.png)

![](assets/20.png)

![](assets/21.png)

# Install Dovecot Server

![](assets/22.png)

![](assets/23.png)

## Last Check

![](assets/24.png)

![](assets/25.png)