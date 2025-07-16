---
layout: split-screen
title: Home
---

## About me:

I’m a PhD student at the university of Toronto working to create advances at the intersection of machine learning and genomics. I am passionate about the subject because the consequences of discovery are so significant - biology is all around us and yet we understand so little of it.

Prior to starting my PhD I worked as a computational biologist at
Deep Genomics where I worked on translating foundational research in machine learning and genomics into pre-clinical applications.

My PhD projects are in the areas of self-supervised contrastive training, and data efficient learning for biological sequences. I am broadly curious and would love to discuss new and ongoing projects.


--- 
--- 

## Research Timeline

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

## Science Communication

<div class="project-cards-container">
    {% for project in site.data.communication %}
        <a href="{{ project.link }}" class="project-card" target="_blank">
            <div class="project-card-image">
                <img src="{{ project.image }}" alt="{{ project.title }}">
            </div>
            <div class="project-card-content">
                <h3>{{ project.title }}</h3>
                <p>{{ project.description }}</p>
            </div>
        </a>
    {% endfor %}
</div>

---
---

## Talks

<div class="project-cards-container">
    {% for talk in site.data.talks %}
        <a href="{{ talk.link }}" class="project-card talk-card" target="_blank">
            <div class="project-card-image">
                <img src="{{ talk.image }}" alt="{{ talk.title }}">
            </div>
            <div class="project-card-content">
                <h3>{{ talk.title }}</h3>
                <p class="project-card-subtitle">{{ talk.subtitle }}</p>
                <p>{{ talk.description }}</p>
            </div>
        </a>
    {% endfor %}
</div>

--- 
--- 

## Misc

<div class="project-cards-container">
    {% for project in site.data.misc %}
        <a href="{{ project.link }}" class="project-card" target="_blank">
            <div class="project-card-image">
                <img src="{{ project.image }}" alt="{{ project.title }}">
            </div>
            <div class="project-card-content">
                <h3>{{ project.title }}</h3>
                <p>{{ project.description }}</p>
            </div>
        </a>
    {% endfor %}
</div>
