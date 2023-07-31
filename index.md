---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

<header class="header">
<h1 class="header-title">Nasheh Annafii</h1>
<p class="header-subtitle">I'am Programmer</p>
</header>
<ul class="nav">
<li class="px-2"><a class="link" href="/about">About</a></li>
<li class="px-2"><a class="link" href="/skill">Skill</a></li>
<li class="px-2"><a class="link" href="/contact">Contact</a></li>
<li class="px-2"><a class="link" href="/social-media">Social Media</a></li>
</ul>
<hr class="hr">
<main>
{% for post in site.posts %}
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
{% endfor %}
</main>