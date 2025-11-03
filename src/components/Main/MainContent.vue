<template>
  <div class="container">
    <div class="hero-section">
      <img :src="bannerImage" alt="Banner image" class="hero-image" />
      <div class="hero-text">
        <p class="label">In Label</p>
        <h2 class="title">Ini Adalah Judul Artikel</h2>
        <p class="author">By Ridho Satriawan</p>
      </div>
    </div>
    
  </div>
</template>

<script setup>
import bannerImage from '@/assets/banner-image.png'
</script>

<style scoped>

.container {
  display: grid;
  justify-content: center;
  align-items: center;
  margin-top: 50px;
}


.hero-section {
  position: relative;
  width: 1200px;
  height: 396px;
}


.hero-image {
  width: 100%;
  height: 100%;
  border-radius: 20px;
  object-fit: cover;
  display: block;

}


.hero-text {
  position: absolute;
  top: 292px;
  left: 70px;
  color: black;
  font-family: Arial, sans-serif;
}


.label {
  font-size: 15px;
  margin: 0;
}

.title {
  font-size: 25px;
  font-weight: bold;
  margin: 2px 0;
}

.author {
  font-size: 13px;
  margin: 0;
}

/* 📱 Адаптация под мобильный экран */
@media screen and (max-width: 768px) {
  .hero-section {
    width: 470px;
    height: 450px;
  }


 

  
  .hero-text{
    width: 355px;
height: 100px;
top: 258px;
left: 46px;


  }
}

</style>
