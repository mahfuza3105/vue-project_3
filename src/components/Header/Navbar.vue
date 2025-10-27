<template>
  <div class="navbar">
    <div class="container">
      <a href="/" class="logo">Yangiliklar</a>

      <ul class="menu">
        <li><a href="#">Mahalliy</a></li>
        <li><a href="#">Jahon</a></li>
        <li><a href="#">Euro 2024</a></li>
        <li><a href="#">Texnalogiya</a></li>
      </ul>

      <button type="button">
        <img :src="searchIcon" alt="Search icon" />
      </button>
    </div>
  </div>
</template>

<script setup>
import searchIcon from './search.png'
</script>

<style scoped>
.navbar {
  background-color: #02A28F;
  color: white;
}

.container {
  margin-left: auto;
  margin-right: auto;
  display: flex;
  max-width: 1160px;
  padding: 16px 13px;
  align-items: center;
}

.logo {
  line-height: 1;
  font-family: Montserrat;
  font-weight: 700;
  font-style: Bold;
  font-size: 36px;
}

.menu {
  align-items: center;
  display: flex;
  column-gap: 25px;
  margin-left: auto;
}

button {
  margin-left: 30px;
  background: none;
  border: none;
  cursor: pointer;
}

@media screen and (max-width: 768px) {
  .menu {
    display: none;
  }

  button {
    margin-left: auto;
  }

  .container {
    padding: 19px 16px;
  }

  .logo {
    font-family: Montserrat;
    font-weight: 500;
    font-style: Medium;
    font-size: 20px;
  }
}
</style>
