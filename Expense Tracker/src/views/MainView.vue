<template>
  <main>
    <div class="container">
      <div class="left-section">
        <a class="logo">
          <img src="@/assets/logo.svg" alt="logo" class="logo-icon">
          <span class="logo-text">Diamond expense tracker</span>
        </a>
        <button class="left-button-active"><img src="@/assets/home-black.svg" alt="home-black"
            class="sidebutton-icon-active"></button>
        <button class="left-button"><img src="@/assets/stats.svg" alt="stats" class="sidebutton-icon"></button>
        <button class="left-button"><img src="@/assets/favorites.svg" alt="favorites" class="sidebutton-icon"></button>
        <button class="left-button"><img src="@/assets/settings.svg" alt="settings" class="sidebutton-icon"></button>
        <button class="light-darkmode-button" @click="toggleDarkMode">
          <div class="dark-slider"
            :style="{ width: isDarkMode ? '50px' : '0', backgroundColor: isDarkMode ? '#FFF' : '#D9D9D9' }"></div>
          <div class="light-slider"
            :style="{ width: isDarkMode ? '0' : '50px', backgroundColor: isDarkMode ? '#D9D9D9' : '#FFF' }"></div>
          <img src="@/assets/dark.svg" alt="Dark Mode Icon" class="dark-icon">
          <img src="@/assets/light.svg" alt="Light Mode Icon" class="light-icon">
        </button>
      </div>
      <div class="divider"></div>
      <div class="right-section">
        <div class="search-bar">
          <input type="text" class="search-input" placeholder="Search Expense">
          <button class="search-button">
            <img src="@/assets/searchblack.svg" alt="Search" class="search-icon">
          </button>
        </div>
        <div class="add-expense">
          <input type="text" class="add-expense-input" placeholder="Add Expense">
          <button class="add-expense-button">
            <img src="@/assets/add.svg" alt="Add" class="add-expense-icon">
          </button>
        </div>

      </div>
    </div>
  </main>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const isDarkMode = ref(false);

function toggleDarkMode() {
  isDarkMode.value = !isDarkMode.value;
}
</script>

<style>
* {
  width: 100%;
  background: #3F4B5B;
}

body {
  overflow: hidden;
  /* Disable scrolling */
}

main {
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  width: 89.58333%;
  /* Adjust as needed */
  max-width: 300vh;
  /* Maximum width */
  height: 80vh;
  /* Adjust as needed */
  max-height: 160vh;
  /* Maximum height */
  border-radius: 20px;
  background: #1F262F;
  display: flex;
}

.left-section {
  margin-left: 3.125%;
  width: 149px;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  background: transparent;
}

.logo-icon {
  width: 55px;
  height: 48px;
  flex-shrink: 0;
}

.logo-text {
  color: #9B51E0;
  font-family: Inter;
  font-size: 14px;
  font-style: normal;
  font-weight: 530;
  line-height: normal;
  background: transparent;
}

.logo {
  width: 90px;
  height: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  /* Adjusted alignment */
  background: transparent;
  font-family: Inter;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  margin-top: 6%;
  /* Adjusted margin from the top of the container */
  margin-bottom: 20%
}

.left-button {
  width: 90px;
  height: 90px;
  background: #D9D9D9;
  border: none;
  flex-shrink: 0;
  border-radius: 20px;
  margin-bottom: 20%;
  cursor: pointer;

}

.left-button-active {
  width: 90px;
  height: 90px;
  background: #FFF;
  border: none;
  flex-shrink: 0;
  border-radius: 20px;

  margin-bottom: 20%;
  cursor: pointer;
}

.sidebutton-icon {
  background: transparent;
}

.sidebutton-icon-active {
  background: transparent;

}

.light-darkmode-button {
  position: relative;
  width: 90px;
  height: 54px;
  flex-shrink: 0;
  border-radius: 20px;
  background: #D9D9D9;
  border: none;
  cursor: pointer;
}

.dark-icon,
.light-icon {
  position: absolute;
  top: 12px;
  width: 30px;
  height: 30px;
}

.dark-icon {
  left: 10px;
  background: transparent;

}

.light-icon {
  right: 10px;
  background: transparent;

}

.dark-slider {
  position: absolute;
  top: 0;
  left: 0;
  width: 50px;
  height: 54px;
  border-radius: 20px;
  transition: transform 0.3s ease;
}

.light-slider {
  position: absolute;
  top: 0;
  left: 40px;
  width: 50px;
  height: 54px;
  border-radius: 20px;
  transition: transform 0.3s ease;

}

.dark-mode .slider {
  transform: translateX(100%);
}

.divider {
  width: 1px;
  height: 100%;
  background-color: white;
}

.right-section {
  padding: 1%;
  border-radius: 20px;
  background: transparent;
}

.search-bar {
  width: 400px;
  height: 90px;
  border-radius: 25px;
  background: #D9D9D9;
  margin-left: 17.4479166667%;
  margin-top: 5.8518518519%;
  float: left; /* Add this line */
}

.search-input {
  width: calc(100% - 150px);
  /* Adjust as needed */
  font-size: xx-large;
  height: 100%;
  border: none;
  border-radius: 25px;
  background: transparent;
  outline: none;
}

.search-button {
  width: auto;
  /* Adjust as needed */
  border: none;
  background: transparent;
  padding-left: 9%;
  cursor: pointer;
}

.search-icon {
  width: 100%;
  background: transparent;
  padding-bottom: 20%;
  padding-left: 9%;
  height: 100%;
}

.add-expense {
  width: 400px;
  height: 90px;
  border-radius: 25px;
  background: #D9D9D9;
  margin-left: 2.08333333333%; /* Adjusted margin-left */
  margin-top: 5.8518518519%;
  float: left; /* Add this line */
}

.add-expense-input {
  width: calc(100% - 150px);
  font-size: xx-large;
  height: 100%;
  border: none;
  border-radius: 25px;
  background: transparent;
  outline: none;
}

.add-expense-button {
  width: auto;
  /* Adjust as needed */
  border: none;
  background: transparent;
  padding-bottom: 20%;
  padding-left: 9%;
  cursor: pointer;
}

.add-expense-icon {
  width: 100%;
  background: transparent;
  padding-bottom: 20%;
  padding-left: 9%;
  height: 100%;
}
</style>
