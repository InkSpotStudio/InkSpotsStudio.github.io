---
layout: post
title: "My First Poem"
date: 2025-10-20
---

<div class="overlay"></div>

<!-- Hamburger Navigation -->
<nav>
  <div class="menu-toggle" onclick="toggleMenu()">☰</div>
  <ul id="menu">
    <li><a href="{{ '/' | relative_url }}">Home</a></li>
    <li><a href="{{ '/poetry' | relative_url }}">Poetry</a></li>
  </ul>
</nav>
<hr>

# My First Poem

Roses are red,<br>
Violets are blue,<br>
GitHub Pages is fun,<br>
And so are you.

---

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
