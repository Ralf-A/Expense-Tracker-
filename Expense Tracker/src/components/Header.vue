<template>
    <header>
        <div class="button-container">
            <div class="months-expenses">
                <span class="months-text">This Month's Expenses:</span>
                <span class="months-amount">520 </span>
                <span class="currency">€</span>
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


            <!-- Settings button -->
            <button class="settings-button">
                <img src="@/assets/burger.svg" alt="burger" class="button-icon">
                <BurgerDropdown />

            </button>
        </div>
    </header>
</template>


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
    /* Use flexbox */
    align-items: center;
    font-size: 26px;
    /* Set the font size to 26px */
    white-space: nowrap;
    /* Prevent text wrapping */

}

.months-text {
    text-align: left;
    margin-left: 5%;
    background: transparent;
}

.months-amount {
    margin-left: 5%;
    /* Push the amount to the right */
    color: #C55151;
    background: transparent;
}

.currency {
    margin-right: 5%;
    text-align: right;
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
    transition: background-color 0.4s ease;


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
    /* Add margin for spacing */
}

.greetings-name {
    font-size: 26px;
    /* Adjust font size */
}

.greetings-text {
    font-size: 26px;
    /* Adjust font size */
}


.settings-button {
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
    transition: background-color 0.4s ease;
}

.expenses-button:hover,
.settings-button:hover {
    background-color: #D9D9D9;
    /* Change button background color on hover */
}</style>
  