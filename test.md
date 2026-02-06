---
layout: default
title: Test Data Files
---

<div class="container">
    <section style="padding: 50px; background: white; margin: 40px 0;">
        <h2>Data Files Test Page</h2>
        
        <h3>Team from _data:</h3>
        <p>Size: {{ site.data.team.size }}</p>
        <ul>
        {% for member in site.data.team %}
            <li>{{ member.name }} - {{ member.role }}</li>
        {% endfor %}
        </ul>
        
        <h3>Publications from _data:</h3>
        <p>Size: {{ site.data.publications.size }}</p>
        <ul>
        {% for pub in site.data.publications %}
            <li>{{ pub.year }}: {{ pub.title }}</li>
        {% endfor %}
        </ul>
    </section>
</div>