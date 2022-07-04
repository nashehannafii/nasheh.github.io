---
layout: 'post'
title: 'Instal LAMP Linux'
date: 2022-02-23 16:00:00 +0700
---

Saya menggunakan ubuntu linux 22.04 LTS.

## 1. Update Repo

```bash
sudo apt update
```

## 2. Instal Apache2

```bash
sudo apt install apache2
```

### Tes

Buka `http://localhost` di browser kalian

## 2. Instal MySQL

```bash
sudo apt install mysql-server
```

## Buka MySql

```bash
sudo mysql
```


## 3. Instal PHP

```bash
sudo apt install php libapache2-mod-php php-mysql
```

### Cek info PHP

Buat file `info.php` dengan cara sebagai berikut:

```bash
sudo nano /var/www/html/info.php
```

Isi dengan kode berikut.

```php
<?php
phpinfo();
```

Simpan dengan ctrl + x -> 'y' -> enter, 

kemudian buka `http://localhost/info.php` di browser kalian


## Selamat Mencoba !!