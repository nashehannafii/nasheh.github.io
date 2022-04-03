---
layout: 'post'
title: 'Membuat User dan Hak Aksesnya MySQL'
date: 2022-02-24 10:00:00 +0700
---

Saya menggunakan ubuntu linux.

## 1. Masuk ke MySQL

```bash
sudo mysql
```

## 2. Buat User

```sql
CREATE USER 'nama_user'@'lokasi_user' IDENTIFIED BY 'password_user';
```

Contoh

```sql
CREATE USER 'nashehannafii'@'localhost' IDENTIFIED BY 'nasheh';
```

## 3. Atur Hak Akses

```sql
GRANT hak_akses ON nama_database.nama_tabel TO 'nama_user'@'lokasi_user';
```

Contoh

```sql
GRANT ALL ON *.* TO 'nashehannafii'@'localhost';
```

* `ALL` berarti memberikan semua hak akses, bisa diganti SELECT, INSERT, UPDATE, dan query lainnya.
* `*` Berarti semua database dan semua tabel.

## 4. Tes

```bash
sudo mysql -u nama_user -p

# Masukkan Password
```