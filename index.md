---
layout: default
title: Home
---

<header style="position: relative; overflow: hidden;">
    <img src="{{ '/images/meditation-banner.jpeg' | relative_url }}" alt="Meditation and Brainwaves" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; opacity: 0.3; z-index: 0;">
    <div class="container" style="position: relative; z-index: 1;">
        <h1>DANSOM Lab</h1>
        <p>Data-driven Neuroscience Of Meditation</p>
        <div class="university">Michigan State University</div>
    </div>
</header>

<div class="container">
    <section id="about">
        <h2>About the Lab</h2>
        
        <div style="display: grid; grid-template-columns: 2fr 1fr; gap: 40px; align-items: start;">
            <!-- Left column: About text -->
            <div>
                <p>The <strong>DANS-OM Lab (Data-driven Neuroscience Of Meditation)</strong> at Michigan State University advances the scientific understanding of meditation through data-driven research. We employ computational neuroscience, advanced signal processing, machine learning, and rigorous experimental psychology to study contemplative practices.</p>
                
                <p style="margin-top: 20px;">Our research focuses on quantifying neural dynamics, and physiological and behavioral effects of meditation using high-density EEG (64-channel wireless) systems and other devices, questionnaires, and advanced data analysis and machine learning. We investigate various meditation techniques including breath-focus meditation and mantra-based meditation through longitudinal studiesof new and expert meditators and examining event-related potentials (P300), oscillatory biomarkers (alpha/theta power, IAF/IAP), and behavioral correlates (MAIA, FFMQ, PSS). Our goal is to establish evidence-based frameworks for meditation practice and states of consciousness through rigorous scientific  inquiry.</p>
                
                <p style="margin-top: 20px;"><strong>Leadership:</strong> The DANSOM Lab is directed by <strong>Dr. Saiprasad Ravishankar</strong> and has evolved from the <a href="https://slim-msu.github.io/" target="_blank">SLIM (Signals, Learning & Imaging) Lab</a>, expanding to focus specifically on contemplative neuroscience and meditation research.</p>
                
                <p style="margin-top: 20px;">We maintain an in-house EEGlab facility equipped with state-of-the-art 64-channel wireless EEG systems, enabling longitudinal studies that track neural changes over weeks and months of meditation practice.</p>
            </div>
            
            <!-- Right column: Neuroplasticity image -->
            <div style="background: #f8f9fa; padding: 20px; border-radius: 8px; border-left: 4px solid #18453B;">
                <h4 style="color: #18453B; margin-bottom: 15px; font-size: 1.1em;">Featured Finding</h4>
                <img src="{{ '/images/neuroplasticity.jpg' | relative_url }}" alt="Long-term Neuroplasticity" style="width: 100%; height: auto; border-radius: 5px; margin-bottom: 15px;">
                <p style="font-size: 0.9em; line-height: 1.5; color: #333;">
                    <strong>Long-term Neuroplasticity:</strong> Six weeks of Hare Krishna mantra meditation showed enhanced alpha power reduction during practice compared to rest, suggesting improved attentional control with consistent practice.
                </p>
                <a href="{{ '/pdfs/Poster_sfn_2025___64_Channels.pdf' | relative_url }}" target="_blank" style="display: inline-block; margin-top: 10px; color: #18453B; text-decoration: none; font-weight: 500;">📄 View Full Poster →</a>
            </div>
        </div>
    </section>
    <section id="research">
        <h2>Research Areas</h2>
        <div class="research-areas">
            <div class="research-card">
                <h4>Exploring Neural Mechanisms and Effects of Contemplative Practices</h4>
                <p>We use advanced spectral analysis, FOOOF decomposition, and machine learning to identify neural biomarkers and understand the transformative effects of sustained contemplative practice.</p>
            </div>
            
            <div class="research-card">
                <h4>Cognitive & Behavioral Changes</h4>
                <p>Examining longitudinal improvements in attention, cognitive processing speed (P300 latency), mindfulness, interoceptive awareness, and stress reduction through controlled meditation interventions lasting 6+ weeks. Understanding how consistent, deep practice leads to lasting neuroplastic changes and enhanced well-being.</p>
            </div>
            
            <div class="research-card">
                <h4>AI 4 Meditation State Detection</h4>
                <p>Using AI & machine learning for real-time identification of meditation state and their patterns. We distinguish authentic meditative states from mind-wandering with goal of enabling neurofeedback.</p>
            </div>
        </div>

        <h3 style="margin-top: 50px;">Key Findings</h3>
        <ul style="margin-left: 30px; margin-top: 20px;">
            <li>Mantra-based meditation produces distinct alpha band modulations compared to breath-focused techniques</li>
            <li>Six weeks of daily practice significantly reduces P300 latency, indicating improved neural processing efficiency</li>
            <li>Meditation enhances interoceptive awareness (MAIA scores) across all technique types</li>
            <li>Individual Alpha Frequency (IAF) increases and Individual Alpha Power (IAP) decreases during meditation, suggesting enhanced attentional control</li>
            <li>Deep learning models with Stationary Wavelet Transform modules successfully classify meditation states with >90% accuracy</li>
            <li>Consistent deep practice is essential for accessing transformative meditative states</li>
        </ul>
    </section>

    <section id="gallery">
        <h2>📸 Gallery</h2>
        <p>Highlights from our lab activities, conference presentations, and research events.</p>
        
        <div class="gallery-grid">
            {% if site.data.gallery %}
                {% for item in site.data.gallery %}
                <div class="gallery-item" onclick="openLightbox('{{ item.image | relative_url }}')">
                    <img src="{{ item.image | relative_url }}" alt="{{ item.title }}">
                    <div class="gallery-caption">
                        <h4>{{ item.title }}</h4>
                        <p>{{ item.description }}</p>
                    </div>
                </div>
                {% endfor %}
            {% endif %}
        </div>
    </section>

<section id="team">
    <h2>Team</h2>
    
    <h3>Principal Investigator</h3>
    <div class="team-grid">
        {% assign pi = site.data.team | where: "category", "PI" %}
        {% for member in pi %}
        <div class="team-member">
            {% if member.image %}
            <img src="{{ member.image | relative_url }}" alt="{{ member.name }}" style="width: 150px; height: 150px; border-radius: 50%; object-fit: cover; margin-bottom: 15px;">
            {% else %}
            <div style="width: 150px; height: 150px; border-radius: 50%; background: #e0e0e0; margin: 0 auto 15px; display: flex; align-items: center; justify-content: center; color: #999; font-size: 3em;">👤</div>
            {% endif %}
            <h4>{{ member.name }}</h4>
            <div class="role">{{ member.role }}</div>
            <p>{{ member.department }}</p>
        </div>
        {% endfor %}
    </div>

    <h3>Lab Members</h3>
    <div class="team-grid">
        {% assign lab_members = site.data.team | where: "category", "Lab Member" %}
        {% for member in lab_members %}
        <div class="team-member">
            {% if member.image %}
            <img src="{{ member.image | relative_url }}" alt="{{ member.name }}" style="width: 150px; height: 150px; border-radius: 50%; object-fit: cover; margin-bottom: 15px;">
            {% else %}
            <div style="width: 150px; height: 150px; border-radius: 50%; background: #e0e0e0; margin: 0 auto 15px; display: flex; align-items: center; justify-content: center; color: #999; font-size: 3em;">👤</div>
            {% endif %}
            <h4>{{ member.name }}</h4>
            <div class="role">{{ member.role }}</div>
            <p>{{ member.department }}</p>
        </div>
        {% endfor %}
    </div>

    <h3>Undergraduate Research Support</h3>
    <div style="background: #f8f9fa; padding: 20px; border-radius: 8px; margin-top: 20px;">
        <p style="margin: 0;">
            {% assign undergrads = site.data.team | where: "category", "Undergrad Support" %}
            {% for member in undergrads %}
                <strong>{{ member.name }}</strong>{% unless forloop.last %}, {% endunless %}
            {% endfor %}
        </p>
    </div>
</section>

<section id="publications">
        <h2>Selected Publications</h2>
        <ul class="publications">
            {% assign sorted_pubs = site.data.publications | sort: 'year' | reverse %}
            {% for pub in sorted_pubs %}
            <li>
                <strong>{{ pub.authors }}.</strong> "{{ pub.title }}," <em>{{ pub.venue }}</em>
                {% if pub.pdf %}
                <br><a href="{{ pub.pdf | relative_url }}" target="_blank">📄 View Poster (PDF)</a>
                {% endif %}
                {% if pub.link and pub.link != "" %}
                <br><a href="{{ pub.link }}" target="_blank">🔗 Link</a>
                {% endif %}
            </li>
            {% endfor %}
        </ul>
    </section>

    <div class="opportunities">
        <h2 style="color: #ff6600; border-color: #ff6600;">🎓 Join Our Lab</h2>
        
        <div class="opportunity-box">
            <h3>PhD Student Positions Available</h3>
            <p><strong>We are actively seeking motivated PhD students</strong> to join the DANSOM Lab. Ideal candidates will have:</p>
            <ul style="margin: 15px 0 15px 30px;">
                <li>Background in neuroscience, computational science, biomedical engineering, psychology, or related fields</li>
                <li>Strong interest in meditation research and contemplative neuroscience</li>
                <li>Experience with signal processing, machine learning, or EEG analysis (preferred but not required)</li>
                <li>Strong programming skills (Python, MATLAB)</li>
            </ul>
            <a href="mailto:{{ site.email }}" class="btn btn-secondary">Apply for PhD Position</a>
        </div>

        <div class="opportunity-box">
            <h3>Summer Research Internships</h3>
            <p><strong>Undergraduate and Master's students</strong> are invited to apply for summer research internships.</p>
            <ul style="margin: 15px 0 15px 30px;">
                <li>Gain hands-on experience with EEG data collection and analysis</li>
                <li>Learn advanced signal processing and machine learning techniques</li>
                <li>Contribute to ongoing meditation neuroscience studies</li>
                <li>Co-author research publications and conference presentations</li>
            </ul>
            <p><strong>Duration:</strong> 8-12 weeks | Remote or In-person<br>
            <strong>Eligibility:</strong> Current undergraduate or Master's students in relevant fields</p>
            <a href="mailto:{{ site.email }}" class="btn btn-secondary">Apply for Summer Internship</a>
        </div>
    </div>

    
    <section id="contact">
        <h2>Contact Us</h2>
        <div class="contact-info">
            <p><strong>For PhD positions, internships, or collaboration inquiries:</strong></p>
            <p>Email: {{ site.email }}</p>
            <p><strong>Lab Director:</strong><br>
            Dr. Saiprasad Ravishankar<br>
            Department of Computational Mathematics, Science and Engineering<br>
            Michigan State University<br>
            East Lansing, MI 48824</p>
        </div>
    </section>
</div>

<!-- Lightbox Modal -->
<div id="lightbox" class="lightbox" onclick="closeLightbox()">
    <span class="lightbox-close">&times;</span>
    <img class="lightbox-content" id="lightbox-img">
</div>