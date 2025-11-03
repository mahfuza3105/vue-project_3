<script setup>
import Navbar from './components/Header/Navbar.vue'
import MainContent from './components/Main/MainContent.vue'
import AppFooter from './components/Footer/AppFooter.vue'
import CardList from './components/card-list/Card-list.vue'
import AnotherpopularNews from './components/Another-popularNews/PopularNews.vue'
</script>

<template>
  <Navbar />

  
  <div class="container">
    <div class="main_section">
      <MainContent />
      <CardList />
  

    </div>
    
    <div class="main-section">
    
    <AnotherpopularNews />
    </div>

  
  
  </div>
  <AppFooter />
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

a {
  text-decoration: none;
  color: inherit;
}

ul {
  list-style-type: none;
}

#app {
  font-family: "Montserrat", sans-serif;
  background-color: #fff;
  color: #222;
}


.main-section {
  display: flex;
  justify-content: center; 
  align-items: flex-start; 
  gap: 20px; 
  max-width: 1200px;
  margin: 30px auto; 
  padding: 0 20px;
}


@media screen and (max-width: 900px) {
  .main-section {
    flex-direction: column;
    align-items: center;
  }
}
.container{
  display: flex;
}
</style>
