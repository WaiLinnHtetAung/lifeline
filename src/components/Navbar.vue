<template>
    <nav class="nav1">
        <div class="navbar-brand">
            <img src="@/assets/images/ll.png" alt="">
            <div>
                <h2>LIFELINE </h2>
                <h3>GROUP OF COMPANIES</h3>
            </div>
        </div>
        <div class="navbar-contact">
            <div class="first-contact">
                <div class="mail">
                    <i class="fa-solid fa-envelope-open"></i>
                    <div class="info-text">inquiry@lifelinemyanmar.com</div>
                </div>
                <div class="phone">
                    <i class="fa-solid fa-phone-volume"></i>
                    <div class="info-text">09 977 195 890</div>
                </div>
            </div>
            <div class="second-contact">
                <div class="fb">
                    <i class="fa-brands fa-square-facebook"></i>
                    <div class="info-text text-decoration-underline pointer">https://www.facebook.com/<br>lifelinemyanmar</div>
                </div>
                <div class="viber">
                    <i class="fa-brands fa-viber"></i>
                    <div class="info-text">09 977 195 890</div>
                </div>
            </div>
        </div>
    </nav>

    <nav class="nav2">
        <div class="menu-items">
            <div class="menu">
                <i class="fa-solid fa-house-chimney"></i>
                <div><router-link to="/">Home</router-link></div>
            </div>
            <div class="menu">
                <div><router-link to="#">About Us</router-link></div>
                <i class="fa-solid fa-sort-down"></i>
                <div class="dropdown">
                    <router-link to="#">Introduction</router-link>
                    <router-link to="#">CEO Message</router-link>
                    <router-link to="#">Vision & Mission</router-link>
                    <router-link to="#">Company Milestones</router-link>
                </div>
            </div>
            <div class="menu">
                <div><router-link to="#">Business</router-link></div>
                <i class="fa-solid fa-sort-down"></i>
                <div class="dropdown">
                    <router-link to="#">Lifeline</router-link>
                    <router-link to="#">Myanmar Booster Distribution</router-link>
                    <router-link to="#">Loyal Lifeline <i class="fa-solid fa-plus text-secondary"></i><i class="fa-solid fa-minus text-secondary"></i>
                        <div class="subMenu text-center">
                            <router-link to="#">Loyal Lifeline</router-link>
                            <router-link to="#">Lifecare Medical Services</router-link>
                        </div>
                    </router-link>
                </div>
            </div>
            <div class="menu">
                <div><router-link to="#">Our Products & Services</router-link></div>
                <i class="fa-solid fa-sort-down"></i>
                <div class="dropdown">
                    <router-link to="#">Products <i class="fa-solid fa-plus text-secondary"></i><i class="fa-solid fa-minus text-secondary"></i>
                        <div class="subMenu text-center">
                            <router-link to="#">Product Catalouge</router-link>
                            <router-link to="#">Promotions</router-link>
                        </div>
                    </router-link>
                    <router-link to="#">Services</router-link>
                </div>
            </div>
            <div class="menu">
                <div><router-link to="#">Partnerships</router-link></div>
                <i class="fa-solid fa-sort-down"></i>
                <div class="dropdown">
                    <router-link to="#">Principles</router-link>
                    <router-link to="#">Hospitals</router-link>
                </div>
            </div>
            <div class="menu">
                <div><router-link to="#">News & Events</router-link></div>
                <i class="fa-solid fa-sort-down"></i>
                <div class="dropdown">
                    <router-link to="#">CSR Activities</router-link>
                    <router-link to="#">News</router-link>
                </div>
            </div>
            <div class="menu">
                <div><router-link to="#">Contact</router-link></div>
            </div>
        </div>
        <div class="language">
            <div class="lang">
                <i class="fa-solid fa-globe"></i> EN
            </div>
        </div>
    </nav>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    .nav1 {
        padding: 25px 15%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .navbar-brand {
        display: flex;
        align-items: center;
    }

    .nav1 img {
        width: 20%;
    }
    .navbar-brand h2 {
        font-weight: bold;
        letter-spacing: 9px;
        color: var(--main-color);
    }

    .navbar-brand h3 {
        font-size: 18px;
    }

    .navbar-contact {
        display: flex;
        gap: 50px;
    }

    .navbar-contact .info-text {
        font-size: 13px;
    }

    .first-contact, .second-contact {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }

    .first-contact {
        gap: 40px;
    }

    .first-contact .mail, .first-contact .phone, .second-contact .fb, .second-contact .viber {
        display: flex;
        justify-content: start;
        align-items: center;
        gap: 15px;
    }

    .navbar-contact i {
        font-size: 20px;
    }

    .fa-square-facebook {
        color: #3b5998;
    }

    .fa-viber {
        color: #8f5db7;
    }


    /* ----------------------menu navbar---------------------- */
    .nav2 {
        padding: 25px 15%;
        display: flex;
        justify-content: space-between;
        background-color: var(--main-color);
        height: 35px;
        
    }

    .nav2 .menu-items {
        display: flex;
        align-items: center;
        gap: 30px;
    }

    .nav2 .menu {
        display: flex;
        justify-content: start;
        align-items: center;
        gap: 10px;
        position: relative;
        padding: 12px 8px;
    }

    .nav2 .menu div a {
        color: #fff;
        font-weight: bold;
        text-decoration: none;
    }

    .nav2 .menu-items i:first-child {
        color: #f18628;
        font-size: 23px;
    }
    .nav2 .menu-items i:not(:first-child) {
        margin-bottom: 8px;
        color: #dfd9d9;
        font-size: 20px;
    }

    .nav2 .language {
        display: flex;
        align-items: center;
        gap: 10px;
    }

    .language .lang {
        background-color:  var(--sec-color);
        padding: 5px 15px;
        border-radius: 3px;
    }

    /* -----------dropdown------------ */
    .menu .dropdown {
        position: absolute;
        top: 100%;
        left: 0%;
        transform: translateY(-1px);
        z-index: 9999;
    }

    .menu:hover {
        background: #72d3f7;
    }
    .menu .dropdown a {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 350px;
        background: #72d3f7;
        position: relative;
        height: 0;
        padding: 0;
        visibility: hidden;
        transition: all .3s ease-in-out;
        position: relative;
    }

    .menu .dropdown .fa-minus {
        display: none;
    }
    .menu:hover .dropdown a {
        height: 50px;
        padding: 15px 10px 15px 25px;
        visibility: visible;
        transition: all .3s ease-in-out;
    }

    .menu:hover .dropdown a:hover {
        background-color: var(--sec-color);
    }

    /* ----------- sub menu dropdown ----------*/
    .menu .dropdown a .subMenu {
        position: absolute;
        top: 0%;
        left: 100%;
    }
    .menu .dropdown a .subMenu a{
        width: 300px;
        background: #72d3f7;
        display: flex;
        transition: all .3s ease-in-out;
        height: 0;
        padding: 0;
        visibility: hidden;
        margin-left: 0;
    }

    .menu:hover .dropdown a:hover .subMenu a {
        height: 50px;
        padding: 15px 0px 15px 25px;
        visibility: visible;
        transition: all .3s ease-in-out;
    }

    .menu:hover .dropdown a:hover .subMenu a:hover {
        border-left: 1px solid var(--main-color);
    }

    .menu:hover .dropdown a:hover .fa-plus {
        display: none;
    }

    .menu:hover .dropdown a:hover .fa-minus {
        display: inline-block;
        padding-top: 10px;
    }

</style>
