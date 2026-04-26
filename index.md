---
layout: split-screen
title: Home
description: "Personal website of Philip Fradkin, a PhD student at the University of Toronto at the intersection of machine learning and genomics. View my research timeline, projects, and talks."
---

## About me:

I'm a cofounder at [BlankBio](https://blank.bio) working to build RNA foundation models at the intersection of machine learning and biology. I am passionate about the field because the consequences of discovery are significant. Biology is all around us, yet we understand so little of it.

Prior to starting BlankBio I did my PhD at the University of Toronto, working on self-supervised learning for biological sequences. Before that I worked as a computational biologist at Deep Genomics, where I translated foundational research in machine learning and genomics into pre-clinical applications.

My interests are in RNA biology and therapeutics, representation learning for biological sequences, and how to make AI tools useful for scientists. I am broadly curious and would love to discuss new and ongoing projects.

--- 
--- 

<h2 id="writing">Writing</h2>

<div class="writing-list">
    {% for post in site.posts %}
    <a href="{{ post.url | relative_url }}" class="writing-entry">
        <div class="writing-date">{{ post.date | date: "%b %Y" }}</div>
        <div class="writing-content">
            <h3 class="writing-title">{{ post.title }}</h3>
            {% if post.description %}
            <p class="writing-excerpt">{{ post.description }}</p>
            {% endif %}
        </div>
    </a>
    {% endfor %}
</div>

---
---

<h2 id="timeline">Research Timeline</h2>

<div class="timeline">
    {% for item in site.data.research_timeline %}
    <div class="timeline-item">
        <div class="timeline-date">{{ item.date }}</div>
        <div class="timeline-content">
            <h3><a href="{{ item.link }}" target="_blank">{{ item.title }}</a></h3>
            {% if item.authors %}
                <p class="timeline-authors">
                {% for author in item.authors %}
                    {% if author contains 'Philip Fradkin' or author contains 'Phil Fradkin' %}
                        <strong>{{ author }}</strong>
                    {% else %}
                        {{ author }}
                    {% endif %}
                    {%- unless forloop.last -%}, {% endunless %}
                {% endfor %}
                </p>
            {% endif %}
            <p class="timeline-publication">{{ item.publication }}</p>
            <p>{{ item.note }}</p>
            {% if item.sub_entries %}
            <div class="timeline-sub-entries">
                {% for sub_item in item.sub_entries %}
                <div class="sub-entry">
                    {% if sub_item.link %}
                        <a href="{{ sub_item.link }}" target="_blank" class="sub-entry-link">
                            <p class="sub-entry-publication">{{ sub_item.publication }}</p>
                            <p>{{ sub_item.note }}</p>
                        </a>
                    {% else %}
                        <p class="sub-entry-publication">{{ sub_item.publication }}</p>
                        <p>{{ sub_item.note }}</p>
                    {% endif %}
                </div>
                {% endfor %}
            </div>
            {% endif %}
        </div>
    </div>
    {% endfor %}
</div>

---
---

<h2 id="science-communication">Science Communication</h2>

<div class="project-cards-container">
    {% for project in site.data.communication %}
        {% include project_card.html item=project %}
    {% endfor %}
</div>

---
---

<h2 id="talks">Talks</h2>

<div class="project-cards-container">
    {% for talk in site.data.talks %}
        {% include project_card.html item=talk type='talk' %}
    {% endfor %}
</div>

--- 
--- 

<h2 id="misc">Misc</h2>

<div class="project-cards-container">
    {% for project in site.data.misc %}
        {% include project_card.html item=project %}
    {% endfor %}
</div>
