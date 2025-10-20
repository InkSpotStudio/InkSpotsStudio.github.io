---
title: "First Poetry Post"
date: 2025-10-20
---

<link rel="stylesheet" href="../assets/css/style.css">

<div class="poem">
Roses are red,<br>
Violets are blue,<br>
Gold shines bright,<br>
In the darkened hue.
</div>

---

## Leave a Comment

<form id="comment-form" method="POST" action="https://inkspotstudio.github.io/staticman/v3/entry/github/inkspotstudio/InkSpotsStudio.github.io/main/comments">
  <label>Name: <input type="text" name="fields[name]" id="name" required></label><br>
  <label>Email: <input type="email" name="fields[email]" required></label><br>
  <label>Comment:<br><textarea name="fields[comment]" rows="4" required></textarea></label><br>
  <button type="submit">Submit</button>
</form>

<script>
// Persist name locally for returning users
const nameInput = document.getElementById('name');
if(localStorage.getItem('poetName')) {
  nameInput.value = localStorage.getItem('poetName');
}
nameInput.addEventListener('input', () => {
  localStorage.setItem('poetName', nameInput.value);
});
</script>

---

## Comments

<ul class="comments-list">
{% for comment in site.data.comments %}
  {% if comment.page == page.url %}
    <li>
      <strong>{{ comment.name }}</strong> said:<br>
      {{ comment.comment | markdownify }}
    </li>
  {% endif %}
{% endfor %}
</ul>
