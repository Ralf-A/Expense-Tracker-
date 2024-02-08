<template>
    <header>
        <div class="button-container">
            <div class="months-expenses">
                <span class="months-text">This Month's Expenses:</span>
                <span class="months-amount">520 </span>
                <span class="currency-header">€</span>
            </div>


            <!-- Home expenses button -->
            <button class="expenses-button">
                <img src="@/assets/home.svg" alt="home" class="button-icon">
                home
            </button>

            <!-- Car expenses button -->
            <button class="expenses-button">
                <img src="@/assets/car.svg" alt="car" class="button-icon">
                car
            </button>

            <!-- Groceries expenses button -->
            <button class="expenses-button">
                <img src="@/assets/groceries.svg" alt="groceries" class="button-icon">
                groceries
            </button>

            <!-- Shopping expenses button -->
            <button class="expenses-button">
                <img src="@/assets/shopping.svg" alt="shopping" class="button-icon">
                shopping
            </button>

            <!-- Other expenses button -->
            <button class="expenses-button">
                <img src="@/assets/other.svg" alt="other" class="button-icon">
                other
            </button>

            <!-- Greetings TODO: name -->
            <div class="greetings">
                <div class="greetings-content">
                    <span class="greetings-text">Hi, </span><span class="greetings-name">Ralf</span>
                </div>
            </div>
            <button class="settings-button" @click.stop="toggleDropdown">
                <img src="@/assets/burger.svg" alt="burger" class="button-icon">

                <div class="dropdown-menu" v-if="isOpen" ref="dropdownMenu">
                    <!-- Currency div with four buttons in 2x2 layout -->
                    <div class="currency-div">
                        <!-- Box with text "Currency:" -->
                        <div class="currency-label">Currency:</div>
                        <!-- Buttons for currencies -->
                        <div class="currency-buttons">
                            <!-- Button for currency £ -->
                            <button class="currency-button">£</button>
                            <!-- Button for currency € -->
                            <button class="currency-button">€</button>
                            <!-- Button for currency $ -->
                            <button class="currency-button">$</button>
                            <!-- Button for currency ¥ -->
                            <button class="currency-button">¥</button>
                        </div>
                    </div>
                    <button class="dropdown-settings-button">
                        Settings
                        <img src="@/assets/settings.svg" alt="settings" class="button-icon">

                    </button>
                    <!-- Log out button -->
                    <button class="dropdown-logout-button">
                        Log out

                        <img src="@/assets/logout.svg" alt="logout" class="button-icon">
                    </button>
                </div>
            </button>

        </div>
    </header>
</template>


<script>
export default {
    data() {
        return {
            isOpen: false
        };
    },
    methods: {
        toggleDropdown() {
            this.isOpen = !this.isOpen;
            // Toggle isOpen when the settings button is clicked
            if (this.isOpen) {
                // If the menu is open, add a click event listener to the body
                document.body.addEventListener('click', this.handleClickOutside);
            } else {
                // If the menu is closed, remove the click event listener from the body
                document.body.removeEventListener('click', this.handleClickOutside);
            }
        },
        handleClickOutside(event) {
            // Check if the clicked element is outside the dropdown menu and its contents
            const dropdownMenu = this.$refs.dropdownMenu;
            if (dropdownMenu && !dropdownMenu.contains(event.target)) {
                // If clicked outside the dropdown menu, close the menu
                this.isOpen = false;
                // Remove the event listener from the body
                document.body.removeEventListener('click', this.handleClickOutside);
            }
        }
    }
};
</script>

<style>
.button-container {
    display: flex;
    padding-bottom: 1.759%;
    align-items: center;
}


.months-expenses {
    width: 417px;
    height: 80px;
    margin-left: 5.20833333333%;
    margin-right: 2.23958333333%;
    flex-shrink: 0;
    color: white;
    border: none;
    border-radius: 10px;
    background: #1F262F;
    display: flex;
    align-items: center;
    font-size: 26px;
    white-space: nowrap;

}

.months-text {
    text-align: left;
    margin-left: 5%;
    background: transparent;
}

.months-amount {
    margin-left: 5%;
    color: #C55151;
    background: transparent;
}

.currency-header {
    margin-left: 1%;
    margin-right: 5%;
    background: transparent;
}


.expenses-button {
    flex-shrink: 0;
    margin-right: 1.04166666667%;
    width: 80px;
    height: 80px;
    color: white;
    border: none;
    border-radius: 10px;
    background: #1F262F;
    cursor: pointer;
    text-align: center;
    font-family: 'Inter', sans-serif;
    font-size: 13.5px;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
}

img {
    width: 46px;
    height: 45px;
    flex-shrink: 0;
    background: transparent;
    vertical-align: middle;

}

.greetings {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-shrink: 0;
    width: 325px;
    margin-left: 16.25%;
    height: 80px;
    color: white;
    border: none;
    border-radius: 10px;
    background: #1F262F;
    font-size: 26px;
    white-space: nowrap;

}

.greetings-content {
    background: #1F262F;
    justify-content: center;
    align-items: center;
}

.greetings-name,
.greetings-text {
    background-color: transparent;
    margin: 0;
}

.greetings-name {
    font-size: 26px;
}

.greetings-text {
    font-size: 26px;
}

.expenses-button:hover,
.settings-button:hover {
    background-color: #D9D9D9;
}

.settings-button {
    position: relative;
    z-index: 998;
    flex-shrink: 0;
    margin-left: 2.23958333333%;
    margin-right: 5.20833333333%;
    width: 80px;
    height: 80px;
    color: white;
    border: none;
    border-radius: 10px;
    background: #1F262F;
    cursor: pointer;
}

.dropdown-menu {
    position: absolute;
    background: white;
    z-index: 999;
    margin-top: 22%;
    margin-left: -364.5%;
    height: 407.5%;
    width: 457.5%;
    border-radius: 20px;
    pointer-events: none;
}

.dropdown-menu * {
    pointer-events: auto;
}


.currency-div {
    margin-top: 1.85%;
    border-radius: 20px;
    background-color: #D9D9D9;
    display: flex;
    width: 96.93%;
    margin-left: 1.535%;
    align-items: center;
}

.currency-label {
    background: transparent;
    color: #000;
    text-align: center;

    font-family: Inter, sans-serif;
    font-size: 30px;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
}

.currency-buttons {
    margin-top: 1%;
    background: transparent;
    display: flex;
    flex-wrap: wrap;
    margin-left: 2%;
    border-radius: 20px;
}

.currency-button {
    width: calc(50% - 2%);
    height: 50px;
    border: none;
    border-radius: 10px;
    background-color: #d9d9d9;
    color: #000;
    text-align: center;
    font-family: Inter, sans-serif;
    font-size: 36px;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
    color: rgb(0, 0, 0);
    /* Text color */
    font-size: 18px;
    cursor: pointer;
    margin-bottom: 2%;
    margin-right: 2%;
    /* Margin between buttons */
    outline: none;
    /* Remove outline */
}



.dropdown-settings-button {
    width: 96.93%;
    height: 50px;
    margin-top: 26%;
    /* Space between currency div and log out button */
    border: none;
    border-radius: 10px;
    background: #D9D9D9;
    /* Text color */
    font-size: 18px;
    /* Font size */
    cursor: pointer;
    outline: none;
    color: #000;
    text-align: center;
    font-family: Inter, sans-serif;
    font-size: 30px;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
}

.dropdown-logout-button {
    width: 96.93%;
    height: 50px;
    margin-top: 1.912568306%;
    border: none;
    border-radius: 10px;
    background: #C55151;
    font-size: 18px;
    margin-bottom: 1.85%;
    cursor: pointer;
    outline: none;
    color: #000;
    text-align: center;
    font-family: Inter, sans-serif;
    font-size: 30px;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
}

.currency-button:hover,
.dropdown-settings-button:hover {
    background-color: #f0f0f0;
}

.dropdown-logout-button:hover {
    background-color: #b13d3d;
}
.button-container {
    transition: padding-bottom 0.4s ease;
}

.months-expenses,
.expenses-button,
.settings-button {
    transition: background-color 0.4s ease;
}

.dropdown-menu {
    transition: opacity 0.4s ease;
}

.currency-button,
.dropdown-settings-button,
.dropdown-logout-button {
    transition: background-color 0.4s ease, color 0.4s ease;
}




</style>
  