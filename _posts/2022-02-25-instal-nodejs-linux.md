---
layout: 'post'
title: 'Instal Node JS Linux'
date: 2022-02-25 13:40:00 +0700
---

Saya menggunakan ubuntu linux.

## 1. Instal Versi LTS

```bash
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install -y nodejs
````

## 2. Instal Versi Terbaru

```bash
curl -fsSL https://deb.nodesource.com/setup_current.x | sudo -E bash -
sudo apt-get install -y nodejs
```

## 3. Cek

```bash
node -v && npm -v
```