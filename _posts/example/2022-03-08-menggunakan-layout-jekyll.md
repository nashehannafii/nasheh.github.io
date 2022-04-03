---
layout: 'post'
title: 'Cara Menggunakan Layout Pada Jekyll'
date: 2022-03-08 11:00:00 +0700
---

Layout digunakan untuk memanggil file tertentu sebagai basis tampilan pada halaman jekyll.

File layout adalah file html yang disimpan pada folder `_layouts`.

Layout dapat digunakan pada `posts` dan `page`.

Contoh file `_layouts/base.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
</head>
<body>
	
	{%raw%}{{ content }}{%endraw%}

</body>
</html>
```

> Kata kunci {%raw%}{{ content }}{%endraw%} digunakan untuk memanggil konten yang menggunakan layout tersebut.

Kemudian gunakan layout tersebut, contoh pada halaman `index.html`.

```markdown
---
layout: 'base'
---

Kontent Beranda
```