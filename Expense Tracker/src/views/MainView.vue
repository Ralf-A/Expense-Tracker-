<template>
  <main>
    <div class="container">
      <div class="left-section">
        <a class="logo">
          <img src="E:\Github\Expense-Tracker-Frontend-\Expense Tracker\src\assets\logo.svg" alt="logo" class="logo-icon">
          <span class="logo-text">Diamond expense tracker</span>
        </a>
        <button class="left-button"><img
            src="E:\Github\Expense-Tracker-Frontend-\Expense Tracker\src\assets\home-black.svg" alt="home-black"
            class="sidebutton-icon"></button>
        <button class="left-button"><img src="E:\Github\Expense-Tracker-Frontend-\Expense Tracker\src\assets\stats.svg"
            alt="stats" class="sidebutton-icon"></button>
        <button class="left-button"><img
            src="E:\Github\Expense-Tracker-Frontend-\Expense Tracker\src\assets\favorites.svg" alt="favorites"
            class="sidebutton-icon"></button>
        <button class="left-button"><img src="E:\Github\Expense-Tracker-Frontend-\Expense Tracker\src\assets\settings.svg"
            alt="settings" class="sidebutton-icon"></button>
        <button class="light-darkmode-button" @click="toggleDarkMode">
          <div class="dark-slider"
            :style="{ width: isDarkMode ? '50px' : '0', backgroundColor: isDarkMode ? '#FFF' : '#D9D9D9' }"></div>
          <div class="light-slider"
            :style="{ width: isDarkMode ? '0' : '50px', backgroundColor: isDarkMode ? '#D9D9D9' : '#FFF' }"></div>
          <img src="E:\Github\Expense-Tracker-Frontend-\Expense Tracker\src\assets\dark.svg" alt="Dark Mode Icon"
            class="dark-icon"
            :style="{ zIndex: isDarkMode ? '2' : '1', backgroundColor: isDarkMode ? '#FFF' : '#D9D9D9' }">
          <img src="E:\Github\Expense-Tracker-Frontend-\Expense Tracker\src\assets\light.svg" alt="Light Mode Icon"
            class="light-icon"
            :style="{ zIndex: isDarkMode ? '1' : '2', backgroundColor: isDarkMode ? '#D9D9D9' : '#FFF' }">
        </button>

      </div>
      <div class="divider"></div>
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
  background: #1F262F;
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
  background-color: #1F262F;
}

.logo {
  width: 90px;
  height: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  /* Adjusted alignment */
  background-color: #1F262F;
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

.sidebutton-icon {
  background: #D9D9D9;
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

}

.light-icon {
  right: 10px;

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
}</style>
