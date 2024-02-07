<template>
    <header>
        <div class="button-container">
            <!-- This Months Expenses TODO add amount -->
            <a class="months-expenses">This Months Expenses: €</a> 

            <!-- Home expenses button -->
            <button class="expenses-button">
                <img src="@/assets/home.svg" alt="home"
                    class="button-icon">
                home
            </button>

            <!-- Car expenses button -->
            <button class="expenses-button">
                <img src="@/assets/car.svg" alt="car"
                    class="button-icon">
                car
            </button>

            <!-- Groceries expenses button -->
            <button class="expenses-button">
                <img src="@/assets/groceries.svg" alt="groceries"
                    class="button-icon">
                groceries
            </button>

            <!-- Shopping expenses button -->
            <button class="expenses-button">
                <img src="@/assets/shopping.svg" alt="shopping"
                    class="button-icon">
                shopping
            </button>

            <!-- Other expenses button -->
            <button class="expenses-button">
                <img src="@/assets/other.svg" alt="other"
                    class="button-icon">
                other
            </button>

            <!-- Greetings TODO: name -->
            <a class="greetings">Hi, </a>

            <!-- Settings button -->
            <button class="settings-button">
                <img src="@/assets/burger.svg" alt="burger"
                    class="button-icon">
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

a{
    text-align: center;
    font-size: 26px;
    display: flex;
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
    align-items: center;

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
    font-family: Inter;
    font-size: 14px;
    font-style: normal;
    font-weight: 600;
    line-height: normal;
    
}

img {
    width: 46px;
    height: 45px;
    flex-shrink: 0;
    background: #1F262F;
    vertical-align: middle; 

}

.greetings {
    flex-shrink: 0;
    width: 325px;
    margin-left: 16.25%;
    height: 80px;
    color: white;
    border: none;
    border-radius: 10px;
    background: #1F262F;
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
    transition: background-color 0.3s ease;
}

.header-button:hover {
    background-color: #2980b9;
    /* Change button background color on hover */
}
</style>
  