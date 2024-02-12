<template>
  <main>
    <div class="container">
      <div class="left-section">
        <a class="logo">
          <img src="@/assets/logo.svg" alt="logo" class="logo-icon">
          <span class="logo-text">Diamond expense tracker</span>
        </a>
        <button class="left-button-active"><img src="@/assets/home-black.svg" alt="home-black"
            class="left-button-icon-active"></button>
        <button class="left-button"><img src="@/assets/stats.svg" alt="stats" class="left-button-icon"></button>
        <button class="left-button"><img src="@/assets/favorites.svg" alt="favorites" class="left-button-icon"></button>
        <button class="left-button"><img src="@/assets/settings.svg" alt="settings" class="left-button-icon"></button>
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
        <div class="recent-expenses">
          <div class="recent-expenses-header">Recent Expenses</div>
          <div class="recent-expenses-content">
            <ul>
              <li>
                <span class="description">McDonald's</span>
                <span class="price">5.22</span>
                <span class="currency">€</span>
              </li>
              <li>
                <span class="description">Description 2</span>
                <span class="price">Price 2</span>
                <span class="currency">€</span>
              </li>
              <li>
                <span class="description">Description 3</span>
                <span class="price">Price 3</span>
                <span class="currency">€</span>

              </li>
              <li>
                <span class="description">Description 4</span>
                <span class="price">Price 4</span>
                <span class="currency">€</span>

              </li>
              <li>
                <span class="description">Description 5</span>
                <span class="price">Price 5</span>
                <span class="currency">€</span>

              </li>
              <li>
                <span class="description">Description 6</span>
                <span class="price">Price 6 </span>
                <span class="currency">€</span>

              </li>
              <li>
                <span class="description">Description 7</span>
                <span class="price">Price 7 </span>
                <span class="currency">€</span>

              </li>

            </ul>
          </div>
        </div>

        <div class="sort-by-date">
          <span class="sort-by-date-header">Sort by Date</span>
          <button id="date-from-button" class="date-button">Select From Date</button>
          <span class="date-text">To</span>
          <button id="date-until-button" class="date-button">Select Until Date</button>
          <button id="search-button" class="date-button">Search</button>
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
  font-family: 'Inter', sans-serif;
  font-size: 12px;
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
  background: transparent;
  margin-top: 6%;
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

.left-button-icon {
  background: transparent;
}

.left-button-icon-active {
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
}

.light-darkmode-button:hover,
.add-expense:hover,
.search-bar:hover,
.left-button:hover {
  transition: background-color 0.4s ease;
  background-color: rgb(242, 242, 240);
}

.light-slider {
  position: absolute;
  top: 0;
  left: 40px;
  width: 50px;
  height: 54px;
  border-radius: 20px;

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
  float: left;
}

.search-input {
  width: calc(100% - 150px);
  font-size: xx-large;
  height: 100%;
  border: none;
  border-radius: 25px;
  background: transparent;
  outline: none;
}

.search-button {
  width: auto;
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
  margin-left: 2.08333333333%;
  margin-top: 5.8518518519%;
  float: left;
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
  height: auto;
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


.recent-expenses {
  width: 37.4375%;
  height: 61.5740740741%;
  margin-left: 17.4479166667%;
  margin-top: 2%;
  background: #D9D9D9;
  border-radius: 25px;
  float: left;
  position: relative;
  /* Needed for absolute positioning of child elements */
}

.recent-expenses-header {
  margin-top: 3.518518519%;
  text-align: center;
  background: transparent;
  color: #443F3F;
  text-align: center;
  font-family: 'Inter', sans-serif;
  font-size: 42px;
  font-style: normal;
  font-weight: 600;
  text-align: left;
  margin-left: 5%;
}


.recent-expenses-content {
  width: 94.139194139%;
  height: 77.019748653%;
  margin-top: 6%;
  flex-shrink: 0;
  border-radius: 25px;
  background: #FFF;
  box-shadow: 0px 2px 2px 0px rgba(0, 0, 0, 0.25);
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  overflow: hidden;
}



.recent-expenses-content ul {
  list-style: none;
  padding: 0;
  background: transparent;
  color: #000;
  text-align: center;
  font-family: 'Inter', sans-serif;
  font-size: 20px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
}

.recent-expenses-content li {
  display: flex;
  /* Use flexbox for layout */
  background: transparent;
  padding: 9px;
  /* Add padding between list items */
  border-bottom: 1px solid #000000;
  /* Add bottom border between list items */
}

.recent-expenses-content li:last-child {
  border-bottom: none;
  /* Remove bottom border from the last list item */
}

.description {
  flex-grow: 1;
  margin-left: 5%;
  text-align: left;
  background: transparent;
  /* Expand to fill available space */
}

.price {
  margin-left: auto;
  /* Push the price to the right */
  text-align: right;
  color: #C55151;
  background: transparent;
  /* Add space between description and price */
}

.currency {
  margin-left: -16%;
  /* Adjust as needed */

  background: transparent;
  /* Add space between price and currency */
}


.sort-by-date {
  width: 13.125%;
  /* Same width as recent expenses */
  height: 51.5740740741%;
  /* Same height as recent expenses */
  margin-left: 5%;
  /* 10% margin from the left */
  margin-top: 2%;
  /* Same margin-top as recent expenses */
  background: #D9D9D9;
  border-radius: 25px;
  float: left;
}
</style>
