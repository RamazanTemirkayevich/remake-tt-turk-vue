<template>
    <header class="header">
        <div class="container">
            <div class="header-nav">
                <div class="header-nav__logo">
                    <img src="@/assets/TTlogo.svg" alt="">
                </div>
                <div class="header-nav__btns">
                    <div class="btns-settings">
                        <img src="@/assets/icons/settings.svg" alt="">
                    </div>
                    <div class="btns-admin">
                        <img src="@/assets/icons/admin.svg" alt="">
                        <p>Log in</p>
                    </div>
                </div>
            </div>
            <div class="header-search">
                <form action="">
                    <div class="header-search__form">
                        <input type="text" placeholder="Search in Turk">
                        <select name="" id="">
                            <option value="">Everywhere</option>
                            <option value=""></option>
                            <option value=""></option>
                        </select>
                        <div class="header-search__form--btn">
                            <img src="@/assets/icons/search.svg" alt="">
                        </div>
                    </div>
                </form>
            </div>
        </div>
    </header>
</template>