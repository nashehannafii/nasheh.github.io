---
layout: post
author: nashehannafii
title: "Install PHP MyAdmin Ubuntu LTS"
tags:
date: "2022-07-05"
---

Saya menggunakan ubuntu linux 22.04 LTS.

Sebelum memulai instalasi PHP MyAdmin, pastikan anda sudah [mengistall LAMP (Linux, Apache, MySql, PHP)](https://nashehannafii.github.io/instal-lamp-linux/), Jika sudah maka akan dilanjutkan dengan panduan dibawah

## 1. Update Repo

```bash
sudo apt update
```

## 2. Instal PHP MyAdmin

```bash
sudo apt install phpmyadmin php-mbstring php-zip php-gd php-json php-curl
```

Apabila ada pilihan web server maka:

Pilih Apache2 [*] dengan menekan 'space'
Kemudian Tab -> Enter


Kemudian lakukan aktivasi

```bash
sudo phpenmod mbstring
```

## 3. Restart Web Server

```bash
sudo systemctl restart apache2
```

### Buka PHP MyAdmin

Buka `http://localhost/phpmyadmin` di browser kalian


## Selamat Mencoba !!