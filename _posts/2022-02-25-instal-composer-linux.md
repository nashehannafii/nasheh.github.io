---
layout: 'post'
title: 'Instal Composer Linux'
date: 2022-02-25 13:00:00 +0700
---

Saya menggunakan elementary os.

## 1. Instal Curl

```bash
sudo apt update && sudo apt install wget php-cli php-zip unzip curl
```

## 2. Download Composer Menggunakan Curl

```bash
curl -sS https://getcomposer.org/installer |php
```

## 3. Pindah Composer Ke Sistem

```bash
sudo mv composer.phar /usr/local/bin/composer
```

## 4. Tes

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