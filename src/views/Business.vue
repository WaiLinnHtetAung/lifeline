<template>
    <div class="business">
        <div class="row">
            <div class="col-lg-3 col-md-4 col-sm-12 p-0">
                <div class="menu  w-100">
                    <router-link to="/business/lifeline" :class="{active: slug == 'lifeline'}">Lifeline</router-link>
                    <router-link to="/business/mbd" :class="{active: slug == 'mbd'}">Myanmar Booster Distribution</router-link>
                    <router-link to="/business/loyal-lifeline" :class="{active: slug == 'loyal-lifeline'}">Loyal Lifeline</router-link>
                    <router-link to="/business/lifecare" :class="{active: slug == 'lifecare'}">Lifecare Medical Service</router-link>
                </div>
            </div>
            <div class="col-lg-9 col-md-8 col-sm-12">
                <div class="content">
                    <div v-if="slug === 'lifeline'"><Lifeline></Lifeline></div>
                    <div v-if="slug === 'mbd'"><Mbd></Mbd></div>
                    <div v-if="slug === 'loyal-lifeline'"><LoyalLifeline></LoyalLifeline></div>
                    <div v-if="slug === 'lifecare'"><Lifecare></Lifecare></div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Lifecare from '../components/business/Lifecare'
import LoyalLifeline from '../components/business/LoyalLifeline'
import Mbd from '../components/business/Mbd'
import Lifeline from '../components/business/Lifeline'
export default {
  components: {
    Lifecare,
    LoyalLifeline,
    Mbd, Lifeline },
        props: ['slug'],
    }
</script>

<style scoped>
    .business {
        padding: 30px 15%;
    }

    .business .menu {
        display: flex;
        flex-direction: column;
        background-color: #e5ecf1;
    }

    .business .menu a {
        text-decoration: none;
        padding: 11px 25px;
        transition: .3s ease;
        color: #000;
    }

    .business .menu a:hover {
        background-color: #3a82a3;
        color: #fff;
    }

    .active {
        background-color: #3a82a3;
        color: #fff !important;
    }

    @media (max-width: 1600px) {
        .business {
            padding: 30px 9%;
        }

        .business .menu a {
            padding: 9px 25px;
            font-size: 14px;
        }
    }

    @media (max-width: 1200px) {
        .business {
            padding: 30px 3%;
        }

        .business .menu a {
            padding: 9px 25px;
            font-size: 14px;
        }
    }
</style>
