<template>
  <div class="container">
    
    <div class="main-content_information">
      <div class="breaking_news">
        <h2 class="news">So’nggi yangiliklar</h2>
      </div>
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
</template>

<script setup>
import bannerImage from '@/assets/banner-image.png'

const cards = [
  {
    image: bannerImage,
    label: 'Xorijiy',
    title: 'Ini Adalah Judul Artikel',
    author: 'By Ridho Satriawan',
    text: 'Apa itu HTML? Buat kamu yang pernah membuat sebuah website pastinya sudah tidak asing lagi dengan yang namanya HTML.'
  },
  {
    image: bannerImage,
    label: 'Mahalliy',
    title: 'Artikel Kedua',
    author: 'By Ridho Satriawan',
    text: 'Apa itu HTML? Buat kamu yang pernah membuat sebuah website pastinya sudah tidak asing lagi dengan yang namanya HTML.'
  },
  {
    image: bannerImage,
    label: 'Texnologiya',
    title: 'Artikel Uch',
    author: 'By Ridho Satriawan',
    text: 'Apa itu HTML? Buat kamu yang pernah membuat sebuah website pastinya sudah tidak asing lagi dengan yang namanya HTML.'
  },
  {
    image: bannerImage,
    label: 'Sport',
    title: 'Yangiliklar Dunyosi',
    author: 'By Ridho Satriawan',
    text: 'Apa itu HTML? Buat kamu yang pernah membuat sebuah website pastinya sudah tidak asing lagi dengan yang namanya HTML.'
  }

]
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 30px;
  transform: scale(1.15); /* увеличиваем весь блок */
  transform-origin: top center; /* чтобы масштабирование было из центра */
}

.main-content_information {
  width: 1000px; /* больше */
  height: 56px; /* выше */
  background-color: #02a28f;
  color: #fff;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center; /* центрируем текст */
  margin-top: 40px;
  text-align: center;
}

.news {
  font-size: 20px; /* оставляем тот же размер */
  font-weight: 600;
  letter-spacing: 0.5px;
}

.card-list {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 30px;
  justify-items: center;
  max-width: 1100px;
}

.card {
  width: 100%;
  max-width: 500px; /* увеличили */
  border-radius: 12px;
  overflow: hidden;
  background: #f9f9f9;
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.12);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  cursor: pointer;
}

.card:hover {
  transform: scale(1.05);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.18);
}

.card-img {
  width: 100%;
  height: 240px; /* увеличили */
  object-fit: cover;
}

.card-info {
  padding: 18px 20px; 
}

.label {
  font-size: 12px;
  color: #02a28f;
  font-weight: 600;
  margin: 0;
}

.title {
  font-size: 16px;
  font-weight: bold;
  margin: 4px 0;
}

.author {
  font-size: 13px;
  color: gray;
}

.text {
  font-size: 14px;
  color: #333;
  margin-top: 6px;
  line-height: 1.4;
}

@media screen and (max-width: 768px) {
  .container {
    transform: none; 
  }

  .main-content_information {
    width: 90%;
    height: 40px;
  }

  .news {
    font-size: 16px;
  }

  .card-list {
    grid-template-columns: 1fr;
    gap: 20px;
  }

  .card {
    width: 90%;
  }

  .card-img {
    height: 160px;
  }

  .text {
    font-size: 13px;
  }
}
</style>
