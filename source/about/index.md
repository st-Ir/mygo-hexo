---
title: MyGO!!!!! Character Gallery
date:
comments: false
---

<style>
.character-gallery {
  font-family: system-ui, -apple-system, 'Segoe UI', Roboto, sans-serif;
  text-align: center;
  padding: 2rem 1rem;
  background: transparent;
}

/* Header */
.gallery-header h2 {
  font-size: 2rem;
  margin-bottom: 0.25em;
  color: var(--highlight-foreground);
}
.gallery-header p {
  font-size: 1.1rem;
  color: var(--highlight-comment);
  margin-bottom: 2rem;
}

/* Main Portraits */
.main-portraits {
  display: flex;
  justify-content: center;
  gap: 1rem;
  flex-wrap: wrap;
  margin-bottom: 2.5rem;
}
.main-portraits img {
  width: 120px;
  cursor: pointer;
  transition: all 0.4s ease;
  border-radius: 12px;
}
.main-portraits img:hover {
  transform: scale(1.08) rotate(-2deg);
  opacity: 0.9;
}

/* Character Card */
.character-grid {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 1.5rem;
}
.character-card {
  background: transparent; /* no border box */
  border-radius: 12px;
  padding: 1rem;
  max-width: 280px;
  display: none;
  text-align: center;
}
.character-card.active {
  display: block;
  animation: fadeIn 0.4s ease;
}
.character-card img {
  width: 100%;
  border-radius: 12px;
  transition: opacity 0.4s ease, transform 0.4s ease;
}
.character-card h3 {
  margin: 0.75rem 0 0.25rem;
  font-size: 1.2rem;
  color: var(--highlight-foreground);
}
.character-card p {
  margin: 0;
  color: var(--highlight-comment);
  font-size: 0.95rem;
}

/* Toggle button */
.alt-toggle {
  margin-top: 0.8rem;
  padding: 0.4rem 0.8rem;
  border: 1px solid var(--blue-2);
  border-radius: 6px;
  background: transparent;
  color: var(--blue-2);
  cursor: pointer;
  font-size: 0.9rem;
  transition: all 0.3s ease;
}
.alt-toggle:hover {
  background: var(--blue-2);
  color: #fff;
}

@keyframes fadeIn {
  from {opacity:0; transform: scale(0.95);}
  to {opacity:1; transform: scale(1);}
}

/* Responsif */
@media (max-width: 600px) {
  .main-portraits img { width: 90px; }
  .character-card { max-width: 90%; }
}

.gallery-masonry {
  display: grid;
  grid-template-columns: repeat(4, 1fr); /* 4 kolom */
  grid-template-rows: repeat(4, 200px);  /* 4 baris fix */
  grid-auto-flow: dense;
  gap: 16px;
}

.gallery-item {
  border-radius: 14px;
  overflow: hidden;
  position: relative;
}

.gallery-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.4s ease, opacity 0.4s ease;
}

.gallery-item img:hover {
  transform: scale(1.05);
  opacity: 0.8;
  cursor: pointer;
}

/* Variasi ukuran */
.gallery-item.wide {
  grid-column: span 2;
}
.gallery-item.tall {
  grid-row: span 2;
}

/* Responsif */
@media (max-width: 768px) {
  .gallery-masonry-wrapper {
    max-height: 100vh; /* default collapse */
    overflow: hidden;
    transition: max-height 0.4s ease;
  }
  .gallery-masonry-wrapper.expanded {
    max-height: none; /* expand penuh */
  }
  .toggle-gallery {
    display: block;
    margin: 1rem auto;
    padding: 0.5rem 1rem;
    border: 1px solid var(--blue-2);
    background: transparent;
    color: var(--blue-2);
    border-radius: 6px;
    cursor: pointer;
  }
}
@media (max-width: 480px) {
  .gallery-masonry {
    grid-template-columns: 1fr 1fr;
    grid-auto-rows: 120px;
  }
}
@media (min-width: 769px) {
  .toggle-gallery { display: none; } /* tombol hanya muncul di mobile */
}

</style>

<img src="https://bang-dream.bushimo.jp/mygo/assets/images/common/logo_mygo.png" style="width:10rem"/>

{% heatMapCard latest no-footer %}

::: info
This is an info box.
:::

<div class="character-gallery">
  <!-- Main Character Portraits -->
  <div class="main-portraits">
    <img src="https://bang-dream.bushimo.jp/mygo/assets/images/common/character/img_pager_soyo.png" alt="Soyo" data-character="soyo" />
    <img src="https://bang-dream.bushimo.jp/mygo/assets/images/common/character/img_pager_anon.png" alt="Anon" data-character="anon" />
    <img src="https://bang-dream.bushimo.jp/mygo/assets/images/common/character/img_pager_tomori.png" alt="Tomori" data-character="tomori" />
    <img src="https://bang-dream.bushimo.jp/mygo/assets/images/common/character/img_pager_taki.png" alt="Taki" data-character="taki" />
    <img src="https://bang-dream.bushimo.jp/mygo/assets/images/common/character/img_pager_rana.png" alt="Rana" data-character="rana" />
  </div>
  <!-- Character Showcase Grid -->
  <div class="character-grid">
    <!-- Soyo -->
    <div class="character-card soyo">
      <img src="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_soyo.png" 
           data-original="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_soyo.png"
           data-alt="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_soyo_02.png"
           alt="Soyo" />
      <h3>Soyo</h3><p>Guitar Player</p>
      <button class="alt-toggle">Show Alternative Look</button>
    </div>

  <!-- Anon -->
  <div class="character-card anon">
    <img src="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_anon.png" 
          data-original="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_anon.png"
          data-alt="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_anon_02.png"
          alt="Anon" />
    <h3>Anon</h3><p>Vocalist</p>
    <button class="alt-toggle">Show Alternative Look</button>
  </div>

  <!-- Tomori -->
  <div class="character-card tomori">
    <img src="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_tomori.png" 
          data-original="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_tomori.png"
          data-alt="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_tomori_02.png"
          alt="Tomori" />
    <h3>Tomori</h3><p>Leader</p>
    <button class="alt-toggle">Show Alternative Look</button>
  </div>

  <!-- Taki -->
  <div class="character-card taki">
    <img src="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_taki.png" 
          data-original="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_taki.png"
          data-alt="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_taki_02.png"
          alt="Taki" />
    <h3>Taki</h3><p>Drummer</p>
    <button class="alt-toggle">Show Alternative Look</button>
  </div>

  <!-- Rana -->
  <div class="character-card rana">
    <img src="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_rana.png" 
          data-original="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_rana.png"
          data-alt="https://bang-dream.bushimo.jp/mygo/assets/images/common/img_chara_rana_02.png"
          alt="Rana" />
    <h3>Rana</h3><p>Bassist</p>
    <button class="alt-toggle">Show Alternative Look</button>
  </div>
  </div>
</div>

***

<div class="extra-gallery">
  <div class="gallery-masonry-wrapper">
    <div class="gallery-masonry">
      <div class="gallery-item"><img src="https://bestdori.com/assets/jp/characters/resourceset/res039010_rip/card_normal.png" alt=""></div>
      <div class="gallery-item tall"><img src="https://bestdori.com/assets/jp/characters/resourceset/res037010_rip/card_normal.png" alt=""></div>
      <div class="gallery-item"><img src="https://bestdori.com/assets/en/characters/resourceset/res036008_rip/card_normal.png" alt=""></div>
      <div class="gallery-item"><img src="https://bestdori.com/assets/jp/characters/resourceset/res036011_rip/card_normal.png" alt=""></div>
      <div class="gallery-item tall"><img src="https://bestdori.com/assets/jp/characters/resourceset/res038012_rip/card_normal.png" alt=""></div>
      <div class="gallery-item tall"><img src="https://bestdori.com/assets/en/characters/resourceset/res038005_rip/card_normal.png" alt=""></div>
      <div class="gallery-item wide"><img src="https://bestdori.com/assets/en/characters/resourceset/res040007_rip/card_normal.png" alt=""></div>
      <div class="gallery-item "><img src="https://bestdori.com/assets/jp/characters/resourceset/res039013_rip/card_normal.png" alt=""></div>
      <div class="gallery-item"><img src="https://bestdori.com/assets/jp/characters/resourceset/res037013_rip/card_normal.png" alt=""></div>
      <div class="gallery-item"><img src="https://bestdori.com/assets/jp/characters/resourceset/res039009_rip/card_normal.png" alt=""></div>
      <div class="gallery-item "><img src="https://bestdori.com/assets/en/characters/resourceset/res038007_rip/card_normal.png" alt=""></div>
      <div class="gallery-item"><img src="https://bestdori.com/assets/en/characters/resourceset/res036004_rip/card_normal.png" alt=""></div>
    </div>
  </div>
  <button class="toggle-gallery">Show More</button>
</div>

<script>
const portraits = document.querySelectorAll(".main-portraits img");
const cards = document.querySelectorAll(".character-card");

// klik potret → tampil card
portraits.forEach(p => {
  p.addEventListener("click", () => {
    const char = p.dataset.character;
    cards.forEach(c => c.classList.remove("active"));
    document.querySelector(".character-card."+char).classList.add("active");
  });
});

// toggle alt look dengan animasi
document.querySelectorAll(".alt-toggle").forEach(btn => {
  btn.addEventListener("click", () => {
    const card = btn.closest(".character-card");
    const img = card.querySelector("img");
    const original = img.getAttribute("data-original");
    const alt = img.getAttribute("data-alt");

    img.style.opacity = "0"; // animasi fade out
    setTimeout(() => {
      if (img.src.endsWith(original.split("/").pop())) {
        img.src = alt;
        btn.textContent = "Show Original Look";
      } else {
        img.src = original;
        btn.textContent = "Show Alternative Look";
      }
      img.style.transform = "scale(1.05)";
      img.style.opacity = "1"; // fade in
      setTimeout(()=> img.style.transform="scale(1)", 400);
    }, 300);
  });
});


const btn = document.querySelector(".toggle-gallery");
const wrap = document.querySelector(".gallery-masonry-wrapper");

btn.addEventListener("click", () => {
  wrap.classList.toggle("expanded");
  if (wrap.classList.contains("expanded")) {
    btn.textContent = "Show Less";
  } else {
    btn.textContent = "Show More";
  }
});
</script>
