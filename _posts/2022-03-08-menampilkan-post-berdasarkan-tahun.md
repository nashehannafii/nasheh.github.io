---
layout: 'post'
title: 'Cara Menampilkan Daftar Postingan Berdasarkan Tahun Pada Jekyll'
date: 2022-03-08 11:30:00 +0700
---

Tampilkan semua postingan menggunakan `for`.

```
{% raw %}{% for post in site.posts %}
{% endfor %}{% endraw %}
```

Simpan tahun postingan pertama dan postingan sebelumnya.

```
{% raw %}{% for post in site.posts %}
    {% capture this_year %}
        {{ post.date | date: "%Y" }}
    {% endcapture %}

    {% capture prev_year %}
        {{ post.previous.date | date: "%Y" }}
    {% endcapture %}
{% endfor %}{% endraw %}
```

Cek jika postingan berada urutan yang pertama, jika iya buat section untuk tahun tersebut.

```
{% raw %}{% for post in site.posts %}
    {% capture this_year %}
        {{ post.date | date: "%Y" }}
    {% endcapture %}

    {% capture prev_year %}
        {{ post.previous.date | date: "%Y" }}
    {% endcapture %}

    {% if forloop.first %}
        <section class="year-section">
            <h2 class="year-title">{{ this_year }}</h2>
    {% endif %}
{% endfor %}{% endraw %}
```

Tampilkan postingan tersebut.

```
{% raw %}{% for post in site.posts %}
    {% capture this_year %}
        {{ post.date | date: "%Y" }}
    {% endcapture %}

    {% capture prev_year %}
        {{ post.previous.date | date: "%Y" }}
    {% endcapture %}

    {% if forloop.first %}
        <section class="year-section">
            <h2 class="year-title">{{ this_year }}</h2>
    {% endif %}
    <article class="post">
    <h3><a class="link" href="{{ post.url }}">{{ post.title }}</a></h3>
    <time class="post-time">{{ post.date | date: "%d %b" }}</time>
    </article>

{% endfor %}{% endraw %}
```

Cek apakah postingan tersebut berada pada urutan terakhir, jika iya maka tutup section untuk tahun tersebut.

Jika tidak cek apakah tahun postingan tersebut tidak sama dengan tahun postingan sebelumnya, jika iya maka tutup section untuk tahun tersebut dan buat section untuk tahun postingan sebelumnya.

```
{% raw %}{% for post in site.posts %}
    {% capture this_year %}
        {{ post.date | date: "%Y" }}
    {% endcapture %}

    {% capture prev_year %}
        {{ post.previous.date | date: "%Y" }}
    {% endcapture %}

    {% if forloop.first %}
        <section class="year-section">
            <h2 class="year-title">{{ this_year }}</h2>
    {% endif %}
    <article class="post">
    <h3><a class="link" href="{{ post.url }}">{{ post.title }}</a></h3>
    <time class="post-time">{{ post.date | date: "%d %b" }}</time>
    </article>

    {% if forloop.last %}
        </section>
    {% else %}
        {% if this_year != prev_year %}
            </section>
            <section class="year-section">
                <h2 class="year-title">{{ prev_year }}</h2>
        {% endif %}
    {% endif %}
{% endfor %}{% endraw %}
```