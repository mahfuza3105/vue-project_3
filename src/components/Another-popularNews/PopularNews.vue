<template>
  <div class="container">
    <div class="popular_news">
      <div class="cards_news">
        <div class="main-content_information">
          <h2 class="news">Mashxur Xabarlar</h2>
        </div>

        
        <div class="card-list">
          <div
            v-for="(card, index) in cards"
            :key="index"
            class="card"
          >
            <img :src="card.image" alt="card image" class="card-img" />
            <div class="card-info">
              <p class="label">{{ card.label }}</p>
              <h3 class="title">{{ card.title }}</h3>
              <p class="author">{{ card.author }}</p>
              <p v-if="card.text" class="text">{{ card.text }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import bannerImage from '@/assets/banner-image.png'

const cards = [
  {
    image: bannerImage,
    title: 'Ini Adalah Judul Artikel',
    author: '22 Agustus 2022'
  },
  {
    image: bannerImage,
    title: 'Ini Adalah Judul Artikel',
    author: '22 Agustus 2022'
  },
  {
    image: bannerImage,
    title: 'Ini Adalah Judul Artikel',
    author: '22 Agustus 2022'
  }
]
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
  transform: scale(0.9); /* Уменьшает весь блок */
  transform-origin: top center; /* Центрирует масштабирование */
}

.main-content_information {
  width: 400px; /* было 500px */
  height: 36px; /* было 40px */
  background-color: #02a28f;
  color: #fff;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 20px;
}

.news {
  font-size: 20px;
  font-weight: 600;
  letter-spacing: 0.5px;
}

.card-list {
  display: flex;
  flex-direction: column;
  gap: 15px;
  max-width: 750px; /* было 900px */
  width: 100%;
}

.card {
  display: flex;
  align-items: stretch;
  background: #ffffff;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 3px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  cursor: pointer;
}

.card:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}

.card-img {
  width: 40%; /* было 45% */
  height: 120px; /* было 150px */
  object-fit: cover;
}

.card-info {
  width: 60%; /* было 55% */
  padding: 15px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.label {
  font-size: 12px;
  color: #02a28f;
  font-weight: 600;
  margin-bottom: 6px;
}

.title {
  font-size: 18px;
  font-weight: 700;
  margin: 4px 0;
}

.author {
  font-size: 13px;
  color: gray;
  margin-bottom: 6px;
}

.text {
  font-size: 14px;
  color: #333;
  margin-top: 8px;
  line-height: 1.4;
}

/* ====== Адаптив ====== */
@media screen and (max-width: 768px) {
  .container {
    display: none;
  }
}
</style>
