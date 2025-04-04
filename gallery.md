---
layout: page
title: Gallery
permalink: /gallery/
---

これまでに撮影した写真の一部を紹介します．

<div class="gallery">
{% for image in site.static_files %}
    {% if image.path contains 'assets/img/gallery' %}
    {% assign image_name = image.path | split: '/' | last %}
    <div class="gallery-item">
        <img src="{{ image.path | relative_url }}" 
             alt="Gallery Image" 
             onclick="openModal(this.src, '{{ image_name }}')"
             data-filename="{{ image_name }}">
    </div>
    {% endif %}
{% endfor %}
</div>

<!-- モーダル -->
<div id="imageModal" class="modal">
    <span class="close" onclick="closeModal()">&times;</span>
    <div class="modal-card">
        <img id="modalImage" class="modal-content">
        <div id="caption"></div>
    </div>
</div>

<script>
function openModal(src, filename) {
    var modal = document.getElementById("imageModal");
    var modalImg = document.getElementById("modalImage");
    var captionDiv = document.getElementById("caption");
    
    // modal.style.display = "block";
    modal.style.display = "flex"; // フレックスボックスで中央揃え
    modalImg.src = src;
    
    // ファイル名からコメントを取得
    {% if site.data.image_comments %}
    var comments = {
        {% for comment in site.data.image_comments %}
        "{{ comment[0] }}": "{{ comment[1] }}"{% unless forloop.last %},{% endunless %}
        {% endfor %}
    };
    
    if (comments[filename]) {
        captionDiv.innerHTML = comments[filename];
        captionDiv.style.display = "block";
    } else {
        captionDiv.style.display = "none";
    }
    {% else %}
    captionDiv.style.display = "none";
    {% endif %}
}

function closeModal() {
    var modal = document.getElementById("imageModal");
    modal.style.display = "none";
}

// モーダル外クリックで閉じる
window.onclick = function(event) {
    var modal = document.getElementById("imageModal");
    if (event.target == modal) {
        modal.style.display = "none";
    }
}
</script>

<style>
.gallery {
    display: grid;
    /* 以下のように変更します */
    /* grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); */
    grid-template-columns: repeat(2, 1fr); /* 2列に設定 */
    gap: 1rem;
    padding: 1rem;
}

.gallery-item {
    overflow: hidden;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    aspect-ratio: 1 / 1; /* 正方形にする */
}

.gallery-item img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    cursor: pointer;
    transition: transform 0.3s ease;
}

.gallery-item img:hover {
    transform: scale(1.05);
}

/* モーダルスタイル */
.modal {
    display: none;
    position: fixed;
    z-index: 1000;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0,0,0,0.9);
    align-items: center;
    justify-content: center; /* 水平方向の中央揃え */
}

.modal-card {
    display: flex;
    flex-direction: column;
    align-items: center; /* 子要素も中央揃え */
    max-width: 90%;
    max-height: 90vh;
    background-color: transparent;
}

.modal-content {
    max-width: 100%;
    max-height: 80vh;
    object-fit: contain;
    margin: 0 auto; /* 画像も中央揃え */
}

.close {
    position: absolute;
    right: 35px;
    top: 15px;
    color: #f1f1f1;
    font-size: 40px;
    font-weight: bold;
    cursor: pointer;
    z-index: 1010;
}

#caption {
    margin-top: 15px;
    color: #fff;
    font-size: 1rem;
    padding: 15px;
    text-align: center;
    max-width: 700px;
    /* background-color: rgba(0, 0, 0, 0.5);
    border-radius: 5px; */
    /* backdrop-filter: blur(5px); */
}
</style>