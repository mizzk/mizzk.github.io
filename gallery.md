---
layout: page
title: Gallery
permalink: /gallery/
---

<p>これまでに撮影した写真をカテゴリー別にまとめています．</p>

<div class="gallery-categories">
{% for category in site.data.gallery_categories %}
    <div class="category-card">
        <a href="/gallery/{{ category.slug }}/">
            <div class="category-thumbnail">
                <img src="{{ category.thumbnail | relative_url }}" alt="{{ category.title }}">
            </div>
            <div class="category-info">
                <h3>{{ category.title }}</h3>
                <p>{{ category.description }}</p>
            </div>
        </a>
    </div>
{% endfor %}
</div>

<style>
.gallery-categories {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 2rem;
    padding: 2rem;
}

.category-card {
    background: white;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    transition: transform 0.3s ease;
}

.category-card:hover {
    transform: translateY(-5px);
}

.category-thumbnail {
    aspect-ratio: 16/9;
    overflow: hidden;
}

.category-thumbnail img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.category-info {
    padding: 1rem;
}

.category-info h3 {
    margin: 0 0 0.5rem 0;
    color: #333;
}

.category-info p {
    margin: 0;
    color: #666;
    font-size: 0.9rem;
}

.category-card a {
    text-decoration: none;
    color: inherit;
}
</style>