---
layout: post
author: nashehannafii
title: "Insert post jekyll using terminal"
tags:
date: "2022-07-05"
---

Saya menggunakan Ubuntu 22.04 LTS.

## 1. Add 'thor' and 'stringex'

tambahkan syntax ini di file ***Gemfile*** 

    gem 'thor'
    gem 'stringex'


## 2. Update Bundle

kemudian lakukan update dengan perintah berikut

```bash
bundle install
```
kemudian nyalakan file dengan

```bash
bundle exec jekyll serve
```

## 3. Buat post melalui terminal

ketik nama file anda setelah 'new':

Contoh

```bash
thor jekyll:new Insert post jekyll using terminal
```

Maka akan terbuat file:
Insert-jekyll-using-terminal


## Selamat mencoba !!