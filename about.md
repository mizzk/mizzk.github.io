---
layout: page
title: About
permalink: /about/
---

<div class="profile-container">
  <img src="/assets/img/about/mizzk_pic.jpg" alt="プロフィール画像" class="profile-image">
  <div class="profile-info">
    <h2>Kota Mizutani</h2>
    <p>京都工芸繊維大学大学院 情報工学専攻</p>
  </div>
</div>


# 研究
コンピュータビジョン研究室に所属し，イベントベースカメラとプロジェクタを用いた形状復元や，キャリブレーション手法の研究を行っています．

# 発表・活動
- [第1回Spatial AI勉強会](https://sainetwork.connpass.com/event/337780/)(2024/12)
    - 「X-maps: Direct Depth Lookup for Event-based Structured Light Systems（CVPRW 2023）」という論文の紹介を行いました．[発表スライドはこちら（SpeakerDeck）](https://speakerdeck.com/spatial_ai_network/x-maps-direct-depth-lookup-for-event-based-structured-light-systems)．


# 趣味・その他
- 写真：高校時代に**県大会1位**，現在も街歩きスナップを続けています．
- バイオリン歴：10年（小学生〜大学まで継続）．
- 自作キーボードやDvorak配列など，入力装置にもこだわりあり．
  <!-- - [キーボードについて](/keyboard/)で詳しく紹介しています． -->
- Minecraft：10年以上同じ街を作り続けています．  
  <!-- - [Minecraft: 街の10年史](/minecraft/)で紹介しています． -->



# リンク
- [GitHub](https://github.com/mizzk)
- [Instagram](https://instagram.com/mizzcreate)

<style>
.profile-container {
  display: flex;
  align-items: center;
  margin-bottom: 2rem;
  flex-wrap: wrap;
}

.profile-image {
  width: 200px;
  height: 200px;
  border-radius: 50%; /* 丸く切り抜く */
  object-fit: cover; /* 画像のアスペクト比を維持 */
  /* border: 4px solid #3498db; 青い枠線 */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* 影をつける */
  margin-right: 2rem;
  margin-bottom: 1rem;
}

.profile-info {
  flex: 1;
  min-width: 300px;
}

.profile-info h2 {
  margin-top: 0;
  margin-bottom: 0.5rem;
  font-size: 1.8rem;
}

.profile-info p {
  margin: 0;
  color: #666;
  font-size: 1.1rem;
}

/* レスポンシブ対応 */
@media (max-width: 768px) {
  .profile-container {
    flex-direction: column;
    align-items: flex-start;
  }
  
  .profile-image {
    margin-right: 0;
    margin-bottom: 1.5rem;
  }
}
</style>