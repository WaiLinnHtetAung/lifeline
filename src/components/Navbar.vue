<template>
    <nav class="nav1">
        <div class="brand pointer" @click="navigate('/')">
            <img src="@/assets/images/ll.png" alt="">
            <h2>
                LIFELINE GROUP OF COMPANIES
            </h2>
        </div>

         <!-- Toggle button for mobile -->
        <v-app-bar-nav-icon @click="drawer = !drawer"  id="mobile-menu"></v-app-bar-nav-icon>

        <div class="social">
            <router-link to="#"><i style="color: #3b5998;" class="fa-brands fa-facebook"></i></router-link>
            <router-link to="#"><i style="color: #8f5db7;" class="fa-brands fa-viber"></i></router-link>
            <router-link to="#"><i style="color: #CD201F;" class="fa-brands fa-youtube"></i></router-link>
            <router-link to="#"><i style="color: #0072b1" class="fa-brands fa-linkedin"></i></router-link>
        </div>
    </nav>
    <v-navigation-drawer app v-model="drawer"  id="drawer" temporary>
        <v-list>
            <v-list-item @click="navigate('/')">
                <v-list-item-title>Home</v-list-item-title>
            </v-list-item>
            <v-list-item @click="navigate('/')">
                <v-list-item-title>About</v-list-item-title>
            </v-list-item>

            <v-list-group value="Users">
                <template v-slot:activator="{ props }">
                    <v-list-item
                    v-bind="props"
                    title="Users"
                    ></v-list-item>
                </template>
        
                <v-list-group value="Admin">
                    <template v-slot:activator="{ props }">
                    <v-list-item
                        v-bind="props"
                        title="Admin"
                    ></v-list-item>
                    </template>
        
                    <v-list-item @click="navigate('/')">
                        <v-list-item-title>1 Admin</v-list-item-title>
                    </v-list-item>
                </v-list-group>
    
                <v-list-item @click="navigate('/')">
                    <v-list-item-title>Modarator</v-list-item-title>
                </v-list-item>
    
            </v-list-group>

        </v-list>


    </v-navigation-drawer>

    <nav class="nav2">
        <div class="menu-items">
            <div class="menu home pointer" :class="{active: currentRoute == '/'}" @click="navigate('/')">
                <i class="fa-solid fa-house-chimney mb-1"></i>
                <div><router-link to="/">Home </router-link></div>
            </div>
            <div class="menu" :class="{active: currentRoute.slice(0,9) == '/about-us'}">
                <div><router-link to="#">About Us</router-link></div>
                <i class="fa-solid fa-sort-down"></i>
                <div class="dropdown">
                    <router-link to="/about-us/introduction">Introduction</router-link>
                    <router-link to="/about-us/ceo-message">CEO Message</router-link>
                    <router-link to="/about-us/vision-mission">Vision & Mission</router-link>
                    <router-link to="/about-us/company-milestone">Company Milestones</router-link>
                    <router-link to="/coming-soon">Distribution Network</router-link>
                    <router-link to="/coming-soon">Regulatory Strength</router-link>
                </div>
            </div>
            <div class="menu" :class="{active: currentRoute.slice(0,9) == '/business'}">
                <div><router-link to="#">Business</router-link></div>
                <i class="fa-solid fa-sort-down"></i>
                <div class="dropdown">
                    <router-link to="/business/lifeline">Lifeline</router-link>
                    <router-link to="/business/mbd">Myanmar Booster Distribution</router-link>
                    <router-link to="#">Loyal Lifeline <i class="fa-solid fa-plus"></i><i class="fa-solid fa-minus text-secondary"></i>
                        <div class="subMenu text-center">
                            <router-link to="/business/loyal-lifeline">Loyal Lifeline</router-link>
                            <router-link to="/business/lifecare">Lifecare Medical Services</router-link>
                        </div>
                    </router-link>
                </div>
            </div>
            <div class="menu" :class="{active: currentRoute.slice(0,8) == '/product' || currentRoute.slice(0,8) == '/service'}">
                <div><router-link to="#" >Our Products & Services</router-link></div>
                <i class="fa-solid fa-sort-down"></i>
                <div class="dropdown">
                    <router-link to="#">Products <i class="fa-solid fa-plus"></i><i class="fa-solid fa-minus text-secondary"></i>
                        <div class="subMenu text-center">
                            <router-link to="/product-service/catalog">Product Catalogue</router-link>
                            <router-link to="/coming-soon">Promotions</router-link>
                        </div>
                    </router-link>
                    <router-link to="/service-promotion/service">Services & Promotions</router-link>
                </div>
            </div>
            <div class="menu" :class="{active: currentRoute.slice(0,12) == '/partnership'}">
                <div><router-link to="#">Partnerships</router-link></div>
                <i class="fa-solid fa-sort-down"></i>
                <div class="dropdown">
                    <router-link to="/partnership/principles">Principles</router-link>
                    <router-link to="/partnership/hospitals">Hospitals</router-link>
                </div>
            </div>
            <div class="menu" :class="{active: currentRoute.slice(0,5) == '/news'}">
                <div><router-link to="#">News & Events</router-link></div>
                <i class="fa-solid fa-sort-down"></i>
                <div class="dropdown">
                    <router-link to="/news-events/csr-activities">CSR Activities</router-link>
                    <router-link to="/coming-soon">Events</router-link>
                    <router-link to="/news-events/news">News</router-link>
                </div>
            </div>
            <div class="menu pointer" @click="navigate('/coming-soon')">
                <div>&nbsp;</div>
                <div><router-link to="/coming-soon">Career</router-link></div>
                <i class="fa-solid fa-sort-down" style="visibility:hidden;"></i>
            </div>
            <div class="menu pointer"  @click="navigate('/coming-soon')">
                <div><router-link to="/contact-us">Contact</router-link></div>
            </div>
        </div>

        <v-menu
        transition="slide-x-transition"
        class="language"
        >
            <template v-slot:activator="{ props }">
                <v-btn
                color="warning"
                v-bind="props"
                class="lang-btn"
                >
                    <i class="fa-solid fa-globe" style="color: #000;"></i> <span class="text-dark ms-2">{{ language }}</span>
                </v-btn>
            </template>

            <v-list>
                <v-list-item class="lang-list" @click="language = 'ENG'">
                    <v-list-item-title>ENG</v-list-item-title>
                </v-list-item>
                <v-list-item class="lang-list" @click="language = 'MM'">
                    <v-list-item-title>MM</v-list-item-title>
                </v-list-item>
            </v-list>
        </v-menu>

    </nav>

    
</template>

<script>
import { ref, computed } from 'vue';
import { useRouter } from 'vue-router';

export default {
    setup() {
        const drawer = ref(false);
        const router = useRouter();
        const language = ref('ENG');
        const currentRoute = ref('');
        const navigate = (route) => {
            router.push(route);
            drawer.value = false; // Close the drawer after navigation (for mobile)
        };

        router.afterEach(to => {
            currentRoute.value = to.path;
        })
        
        return {navigate, drawer, language, currentRoute}
    }
}



</script>

<style scoped>
    .nav1 {
        padding: 10px 15%;
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 15px;
        background: #fff !important;
        height: 120px;
    }

    .nav1 .brand {
        display: flex;
        align-items: center;
        gap: 15px;
    }

    #mobile-menu {
        display: none;
    }
    .nav1 img {
        width: 150px;
        height: 150px;
        object-fit: contain;
    }
    
    .nav1 h2 {
        font-weight: bold;
        color: var(--main-color);
    }

    .nav1 .social a {
        margin-left: 15px;
    }

    .nav1 .social a i {
        font-size: 30px;
        transition: .2s ease;
    }

    .nav1 .social a i:hover {
        transform: translateY(-6px);
    }


    /* ----------------------menu navbar---------------------- */
    .nav2 {
        padding: 23px 15%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        background-color: #01579B;
        height: 30px;
        position: sticky;
        top: 0;
        z-index: 9999;
    }

    .nav2 .menu-items {
        display: flex;
        align-items: center;
        gap: 15px;
    }

    .nav2 .menu {
        display: flex;
        justify-content: start;
        align-items: center;
        gap: 10px;
        position: relative;
        padding: 9px 8px;
    }

    .nav2 .menu div a {
        color: #fff;
        font-weight: bold;
        text-decoration: none;
        font-size: 14px;
    }

    .fa-house-chimney {
        color: var(--sec-color) !important;
        font-size: 22px !important;
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

    .v-menu.language {
        z-index: 999999 !important;
    }

    .v-list-item {
        min-height: 20px !important;
        cursor: pointer;
    }

    .v-list-item:hover {
        background: #c2c2c2 !important;
    }

    .v-list-item:hover span {
        color: #fff !important;
    }

    .home {
        padding: 10px 10px !important;
    }

    /* -----------dropdown------------ */
    .menu .dropdown {
        position: absolute;
        top: 100%;
        left: 0%;
        transform: translateY(-1px);
        z-index: 9999;
    }

    .menu:hover{
        background: #E1F5FE;
    }

    .active {
        background: #E1F5FE;
    }

    .menu.active div a {
        color: #000;
    }

    .menu:hover .fa-house-chimney {
        color: var(--sec-color) !important;
    }
    
    .menu:hover div a {
        color: #000;
    }
    .menu .dropdown a {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 350px;
        background: #E1F5FE;
        position: relative;
        height: 0;
        padding: 0;
        visibility: hidden;
        transition: height .3s ease;
        position: relative;
        font-weight: 400 !important;
    }

    .menu .dropdown .fa-plus {
        color: var(--sec-color);
    }

    .menu .dropdown .fa-minus {
        display: none;
    }
    .menu:hover .dropdown a {
        height: 45px;
        padding: 15px 10px 15px 10px;
        visibility: visible;
        transition: all .3s ease-in-out;
        color: #000;
    }

    .menu:hover .dropdown a:hover {
        background-color: #B3E5FC;
        margin-left: 3px;
    }

    /* ----------- sub menu dropdown ----------*/
    .menu .dropdown a .subMenu {
        position: absolute;
        top: 0%;
        left: 100%;
    }
    .menu .dropdown a .subMenu a{
        width: 300px;
        background: #E1F5FE;
        display: flex;
        transition: all .3s ease-in-out;
        height: 0;
        padding: 0;
        visibility: hidden;
        margin-left: 0;
    }

    .menu:hover .dropdown a:hover .subMenu a {
        height: 45px;
        padding: 15px 0px 15px 25px;
        visibility: visible;
        transition: all .3s ease-in-out;
    }

    .menu:hover .dropdown a:hover .subMenu a:hover {
        border-left: 1px solid var(--sec-color);
    }

    .menu:hover .dropdown a:hover .fa-plus {
        display: none;
    }

    .menu:hover .dropdown a:hover .fa-minus {
        display: inline-block;
        padding-top: 10px;
        color: var(--sec-color) !important;
    }


    @media (max-width:1600px) {
        .nav1 {
            padding: 10px 9%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 10px;
            background: #fff !important;
            height: 85px;
        }
        .nav1 img {
            width: 100px;
            height: 100px;
            object-fit: contain;
        }
        
        .nav1 h2 {
            font-weight: bold;
            color: var(--main-color);
            font-size: 25px;
        }
    
        .nav1 .social a i {
            font-size: 25px;
            transition: .2s ease;
        }
    
        /* ----------------------menu navbar---------------------- */
        .nav2 {
            padding: 15px 9%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: #21538b;
            height: 35px !important;
            position: sticky;
            top: 0;
            z-index: 9999;
            margin-top: -2px;
        }
    
        .nav2 .menu-items {
            display: flex;
            align-items: center;
            gap: 5px;
        }
    
        .nav2 .menu {
            display: flex;
            justify-content: start;
            align-items: center;
            gap: 5px;
            position: relative;
            padding: 6px 8px;
        }
    
        .nav2 .menu div a {
            color: #fff;
            font-weight: bold;
            text-decoration: none;
            font-size: 13px;
        }
    
        .fa-house-chimney {
            font-size: 16px !important;
        }
        .nav2 .menu-items i:not(:first-child) {
            margin-bottom: 7px;
            color: #dfd9d9;
            font-size: 15px;
        }

        .lang-btn {
            width: 80px;
            height: 27px !important;
        }

        .v-list-item {
            max-height: 27px !important;
        }
    
        .v-list-item:hover {
            background: #c2c2c2 !important;
        }
    
        .v-list-item:hover span {
            color: #fff !important;
        }

        .home {
            padding: 5.5px 10px !important;
        }
    
        /* -----------dropdown------------ */
        
        .menu:hover div a {
            color: #000;
        }
        .menu .dropdown a {
            width: 230px;
        }
        .menu:hover .dropdown a {
            height: 32px;
            padding: 15px 10px 15px 10px;
            visibility: visible;
            transition: all .3s ease-in-out;
            color: #000;
        }

        .active {
            background: #E1F5FE;
        }
    
        .menu.active div a {
            color: #000;
        }
    
        /* ----------- sub menu dropdown ----------*/
        .menu .dropdown a .subMenu a{
            width: 230px;
        }
    
        .menu:hover .dropdown a:hover .subMenu a {
            height: 32px;
            padding: 15px 0px 15px 25px;
        }
    
    }

    @media (max-width: 1200px) {
        .nav1 {
            padding: 10px 3%;
            gap: 10px;
            height: 85px;
        }
        .nav1 img {
            width: 90px;
            height: 90px;
            object-fit: contain;
        }
        
        .nav1 h2 {
            font-weight: bold;
            color: var(--main-color);
            font-size: 23px;
        }
    
        .nav1 .social a i {
            font-size: 25px;
            transition: .2s ease;
        }
    
        /* ----------------------menu navbar---------------------- */
        .nav2 {
            padding: 15px 3%;
            height: 35px !important;
        }
    
        .nav2 .menu-items {
            gap: 0px;
        }
    
        .nav2 .menu {
            gap: 5px;
            position: relative;
            padding: 6px 8px;
        }
    
        .nav2 .menu div a {
            font-size: 12px;
        }
    
        .fa-house-chimney {
            font-size: 14px !important;
            margin-top: 2px;
        }
        .nav2 .menu-items i:not(:first-child) {
            margin-bottom: 3px;
            color: #dfd9d9;
            font-size: 15px;
        }

    }

    @media (max-width: 490px) {
        .nav1 .brand h2 {
            display: none;
        }

        .nav1 .social {
            display: none;
        }

        #mobile-menu {
            display: inline-block;
        }

        .nav2 {
            display: none;
        }
    }

</style>
