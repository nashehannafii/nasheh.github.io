---
layout: 'post'
title: 'Cara Include Pada Jekyll'
date: 2022-02-25 14:00:00 +0700
---

Include digunakan untuk memanggil file tertentu.

Contohnya untuk memanggil potongan bagian website seperti navbar, sidebar, footer, dsb.

File yang dapat di-include adalah file yang berada di folder `_includes` pada root project jekyll.

Buat sebuah file, contoh `navbar.html`.

```html
<nav>
	<a href="">Brand</a>
	<ul>
		<li>About</li>
		<li>Contact</li>
	</ul>
</nav>
```

Kemudian panggil file `navbar.html` menggunakan include pada file `index.html`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<title>Document</title>
</head>
<body>
	
	{% raw %}{% include navbar.html %}{% endraw %}

	<h1>Beranda</h1>
	<p>Konten</p>
	
</body>
</html>
```