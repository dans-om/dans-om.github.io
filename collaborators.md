---
layout: default
title: Collaborators
---

<header>
    <div class="container">
        <h1>Collaborators</h1>
        <p>Research Partners & Collaborating Scientists</p>
    </div>
</header>

<div class="container">
    <section>
        <h2>Our Collaborative Network</h2>
        <p>The DANSOM Lab works with leading researchers and institutions across multiple disciplines to advance meditation science.</p>
        
        <div class="team-grid" style="margin-top: 40px;">
            {% assign collaborators = site.data.team | where: "category", "Collaborator" %}
            {% for member in collaborators %}
            <div class="team-member">
                {% if member.image %}
                <img src="{{ member.image | relative_url }}" alt="{{ member.name }}" style="width: 150px; height: 150px; border-radius: 50%; object-fit: cover; margin-bottom: 15px;">
                {% else %}
                <div style="width: 150px; height: 150px; border-radius: 50%; background: #e0e0e0; margin: 0 auto 15px; display: flex; align-items: center; justify-content: center; color: #999; font-size: 3em;">👤</div>
                {% endif %}
                {% if member.url %}
                <h4><a href="{{ member.url }}" target="_blank" style="color: #18453B; text-decoration: none;">{{ member.name }}</a></h4>
                {% else %}
                <h4>{{ member.name }}</h4>
                {% endif %}
                <div class="role">{{ member.role }}</div>
                <p>{{ member.department }}</p>
            </div>
            {% endfor %}
        </div>

        <h3 style="margin-top: 50px;">Institutional Partners</h3>
        <div class="research-areas">
            
            <div class="research-card">
                <h4>Brainwave Science, Inc.</h4>
                <p>EEG Technology Development & Signal Processing Research</p>
            </div>
            
            <div class="research-card">
                <h4>Harmony Collective</h4>
                <p>Expert meditation instruction and community practice support (Ypsilanti, MI)</p>
            </div>
        </div>
    </section>
</div>