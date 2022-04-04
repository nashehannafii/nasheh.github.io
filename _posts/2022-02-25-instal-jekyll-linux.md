---
layout: 'post'
title: 'Instal Jekyll Linux'
date: 2022-02-25 13:45:00 +0700
---

Saya menggunakan ubuntu linux.

## 1. Instal Ruby DLL

```bash
sudo apt-get install ruby-full build-essential zlib1g-dev
````

## 2. Setup Ruby Gems

```bash
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

## 3. Instal Jekyll Bundler

```bash
gem install jekyll bundler
```

## 4. Cek

```bash
jekyll -v
````