---
layout: home
title: Ink Spots
---

<!-- Hamburger Navigation -->
<nav>
  <div class="menu-toggle" onclick="toggleMenu()">☰</div>
  <ul id="menu">
    <li><a href="{{ '/' | relative_url }}">Home</a></li>
    <li><a href="{{ '/poetry' | relative_url }}">Poetry</a></li>
    <li><a href="{{ '/about' | relative_url }}">About</a></li>
  </ul>
</nav>
<hr>

# Welcome to Ink Spots

Here, I share my poems, reflections, and creative writings. Dive in and enjoy the journey.

---

## Featured Poems

{% for post in site.posts %}
<section>
### [{{ post.title }}]({{ post.url | relative_url }})
<p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
<a href="{{ post.url | relative_url }}">Read full poem</a>
</section>
{% endfor %}

<hr>

## Leave a Comment

<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
  <label>Name: <input type="text" name="name" required></label><br><br>
  <label>Phone: <input type="text" name="phone"></label><br><br>
  <label>Comment:<br><textarea name="message" rows="4" required></textarea></label><br><br>
  <button type="submit">Submit</button>
</form>

<script>
function toggleMenu() {
  const menu = document.getElementById('menu');
  menu.style.display = (menu.style.display === 'block') ? 'none' : 'block';
}
</script>
