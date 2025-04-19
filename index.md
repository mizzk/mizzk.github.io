---
layout: page
# title: Home
permalink: /
---

<div class="hero">
    <div class="hero-content">
        <h1>Welcome to My Page</h1>
        <p class="hero-description">研究・写真・個人開発など，興味のあることなど</p>
    </div>
    <img src="/assets/img/index/home_pc.jpg" alt="サイトの代表画像" class="hero-image">
</div>

<div class="content-grid">
    <div class="content-card">
        <h2>About</h2>
        <p>私についての情報をまとめています．</p>
        <a href="/about/" class="card-link">Aboutを見る →</a>
    </div>
    <div class="content-card">
        <h2>Gallery</h2>
        <p>これまでに撮影した写真をカテゴリー別にまとめています．</p>
        <a href="/gallery/" class="card-link">Galleryを見る →</a>
    </div>
    <div class="content-card">
        <h2>Apps</h2>
        <p>個人開発したアプリやプロジェクトを紹介しています．</p>
        <a href="/apps/" class="card-link">Appsを見る →</a>
    </div>
</div>

<style>
.hero {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 2rem;
    margin: 2rem 0;
    padding: 2rem;
    text-align: center;
}

.hero-content {
    max-width: 800px;
}

.hero h1 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    color: #333;
}

.hero-description {
    font-size: 1.2rem;
    color: #666;
    line-height: 1.6;
}

.hero-image {
    max-width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.content-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    padding: 2rem;
    max-width: 1200px;
    margin: 0 auto;
}

.content-card {
    background: white;
    border-radius: 8px;
    padding: 2rem;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.content-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
}

.content-card h2 {
    color: #333;
    margin-bottom: 1rem;
}

.content-card p {
    color: #666;
    margin-bottom: 1.5rem;
    line-height: 1.6;
}

.card-link {
    display: inline-block;
    color: #007bff;
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s ease;
}

.card-link:hover {
    color: #0056b3;
}

@media (max-width: 768px) {
    .hero {
        padding: 1rem;
    }
    
    .hero h1 {
        font-size: 2rem;
    }
    
    .content-grid {
        grid-template-columns: 1fr;
        padding: 1rem;
    }
}
</style>
