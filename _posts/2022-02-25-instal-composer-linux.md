---
layout: 'post'
title: 'Instal Composer Linux Ubuntu 22.04 LTS'
date: 2022-02-25 13:00:00 +0700
---

Saya menggunakan Ubuntu 22.04 LTS.

## 1. Instal Curl

Update

```bash
sudo apt update
```
Install wget - php - zip - curl

```bash
sudo apt install wget php-cli php-zip unzip curl
```


## 2. Download Composer Menggunakan Curl dan Setting File Composer

```bash
cd ~
curl -sS https://getcomposer.org/installer -o /tmp/composer-setup.php
```

```bash
HASH=`curl -sS https://composer.github.io/installer.sig`
```

```bash
php -r "if (hash_file('SHA384', '/tmp/composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
```

## 3. Install Composer

```bash
sudo php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer
```


## 4. Testing Composer

```bash
composer
```

```
   ______
  / ____/___  ____ ___  ____  ____  ________  _____
 / /   / __ \/ __ `__ \/ __ \/ __ \/ ___/ _ \/ ___/
/ /___/ /_/ / / / / / / /_/ / /_/ (__  )  __/ /
\____/\____/_/ /_/ /_/ .___/\____/____/\___/_/
                    /_/
Composer version 2.2.6 2022-02-04 17:00:38
```

## Selamat Mencoba !!