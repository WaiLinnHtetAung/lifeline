<template>
    <div class="bg-img">
        <div class="info">
            <h2>1000+</h2>
            <p>Products</p>
            <div></div>
        </div>
        <div class="info">
            <h2>35+</h2>
            <p>Partnerships</p>
            <div></div>
        </div>
        <div class="info">
            <h2>20</h2>
            <p>Hospitals</p>
            <div></div>
        </div>
        <div class="info">
            <h2>500+</h2>
            <p>Pharmacy</p>
            <div></div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    .bg-img {
        margin: 40px auto 100px;
        width: 100%;
        height: 400px;
        background-image: url("../assets/images/info-desk3.webp");
        background-position: center center;
        background-size:100% auto;
        background-repeat: no-repeat;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 250px;
    }

    .bg-img .info h2, .bg-img .info p {
        color: #fff;
        font-weight: bold;
    }

    .info h2 {
        font-size: 44px;
    }

    .info {
        text-align: center;
    }

    .info div {
        border-top: 3px solid var(--sec-color);
    }


</style>
