---
layout: 'post'
title: 'Instal LAMP Linux'
date: 2022-02-23 16:00:00 +0700
---

Saya menggunakan ubuntu linux.

## 1. Update Repo

```bash
sudo apt update
```

## 2. Instal Apache2

```bash
sudo apt install apache2
```

### Tes

Buka `http://ip_mu` atau `http://localhost`

## 2. Instal MySQL

```bash
sudo apt install mysql-server
```

### Run MySQL Secure Instalation

```bash
sudo mysql_secure_installation
```

Ikuti langkah-langkahnya.

### Tes

```bash
sudo mysql
```

## 3. Instal PHP

```bash
sudo apt install php libapache2-mod-php php-mysql
```

### Tes

Buat file `info.php`

```bash
sudo nano /var/www/html/info.php
```

Isi dengan kode berikut.

```php
<?php
phpinfo();
```

Simpan, kemudian buka `http://ip_mu/info.php` atau `http://localhost/info.php`