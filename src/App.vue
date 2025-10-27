<script setup>
import Navbar from './components/Header/Navbar.vue';
import MainContent from './components/Main/MainContent.vue'; 
import AppFooter from './components/Footer/AppFooter.vue'; 
</script>

<template>
    <Navbar />
    <MainContent />
    <AppFooter />
</template>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap');
*{
  margin: 0;
  padding: 0;

}
a{
  text-decoration: none;
  color: inherit;
  font: inherit;
}
ul{
  list-style-type: none;
  text-decoration: none;
}
li{
  text-decoration: none;
}
#app{
  font-family: "Montserrat", sans-serif;
  font-weight: 400;
  box-sizing: border-box;


}
</style>
