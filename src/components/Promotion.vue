<template>
    <div class="promotion">
        <div class="promotion-card">
            <div class="promo-text">
                <div class="horn1">
                    <i class="fa-solid fa-bullhorn"></i>
                </div>
                <h2>Special Promotion</h2>
                <p>Discover the power of healing with our advanced medicine for a healthier tomorrow!</p>
                <router-link to="#" class="btn">View Promotion</router-link>
                <div class="horn2">
                    <i class="fa-solid fa-bullhorn"></i>
                </div>
            </div>
            <div class="promo-img text-end">
                <img src="@/assets/images/promotion.png" alt="">
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    .promotion {
        padding: 80px 15%;
    }

    .promotion-card {
        border-top: 10px solid var(--sec-color);
        height: 350px;
        width: 100%;
        background-image: linear-gradient(to bottom, rgb(162,215,234), rgb(254,138,37, .8));
        display: flex;
        justify-content: space-between;
    }

    .promotion-card .promo-text {
        padding: 60px 40px 30px 80px;
        width: 650px;
        position: relative;
    }

    .promo-text h2 {
        display: inline-flex;
        background: #9c02ae;
        padding: 10px 20px;
        font-size: 20px;
        color: #fff;
        font-weight: bold;
        margin: 0 0 30px 30%;
    }

    .promo-text p {
        font-size: 22px;
        color: #fff;
        line-height: 40px;
    }

    .promo-text .btn {
        background: var(--main-color);
        color: #fff;
    }

    .promotion-card img {
        width: 80%;
    }

    .horn1 i, .horn2 i {
        font-size: 30px;
    }

    .horn1, .horn2 {
        width: 65px;
        height: 65px;
        background: var(--main-color);
        border-radius: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        position: absolute;
    }

    .horn1 {
        top: 10%;
    }
    .horn2 {
        left: 80%;
        bottom: 10%;
        transform: scaleX(-1);
    }
</style>
