---
layout: default
title: Things I'm Reading
---

<div class="favorites-section">
    <h2>All-Time Favorites</h2>
    <ul class="favorites-list">
        {% for fav in site.data.reading_list.favorites %}
            <li><strong>{{ fav.title }}</strong> by {{ fav.author }}</li>
        {% endfor %}
    </ul>
</div>

---

## Reading Log

<div class="book-list">
    {% for book in site.data.reading_list.books reversed %}
        <div class="book-card">
            <div class="book-card-header">
                <h3 class="book-title">{{ book.title }}</h3>
                <span class="book-rating">{{ book.rating }}</span>
            </div>
            <p class="book-author">by {{ book.author }} - <span class="book-date">{{ book.date }}</span></p>
            {% if book.notes %}
                <ul class="book-notes">
                    {% for note in book.notes %}
                        <li>{{ note }}</li>
                    {% endfor %}
                </ul>
            {% endif %}
        </div>
    {% endfor %}
</div>