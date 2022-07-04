---
layout: 'post'
title: 'Membuat User dan Hak Aksesnya MySQL'
date: 2022-02-24 10:00:00 +0700
---

Saya menggunakan ubuntu linux 22.04 LTS.

## 1. Masuk ke MySQL

```bash
sudo mysql
```

## 2. Buat User

```sql
CREATE USER 'nasheh'@'localhost' IDENTIFIED BY 'password';
```
Nb : 

## 3. Atur Hak Akses


```sql
GRANT ALL PRIVILEGES ON *.* TO 'nasheh'@'localhost' WITH GRANT OPTION;
```

* `ALL` berarti memberikan semua hak akses, bisa diganti SELECT, INSERT, UPDATE, dan query lainnya.
* `*` Berarti semua database dan semua tabel.

## 4. Terima Hak Akses

```sql
FLUSH PRIVILEGES;
```


## 5. Selesai

```bash
sudo mysql -u nama_user -p
```

## Akun yang dibuat diatas: 
username    : nasheh

password    : password
# Masukkan Password
```