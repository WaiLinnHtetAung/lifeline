<template>
    <div class="our-business">
        <div class="section-header">
            <div>Business Provided for You</div>
            <h2>OUR BUSINESS</h2>
        </div>

        <div class="business">
            <div class="row">
                <div class="col-lg-3 col-md-6 mb-3 p-1">
                    <div class="business-card">
                        <img src="@/assets/images/ll.png" alt="">
                        <h2>Lifeline</h2>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Illum natus nisi commodi ut optio obcaecati eius modi! Officiis, laudantium in. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Accusamus, sed?</p>
                        <button class="btn btn-warning">See More</button>
                    </div>
                </div>
                <div class="col-lg-3 col-md-6 mb-3 p-1">
                    <div class="business-card">
                        <img src="@/assets/images/mbd.png" alt="">
                        <h2>Myanmar Booster Destribution</h2>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Illum natus nisi commodi ut optio obcaecati eius modi! Officiis, laudantium in. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Accusamus, sed?</p>
                        <button class="btn btn-warning">See More</button>
                    </div>
                </div>
                <div class="col-lg-3 col-md-6 mb-3 p-1">
                    <div class="business-card">
                        <img src="@/assets/images/loyan-lifeline.png" alt="">
                        <h2>Loyal Lifeline</h2>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Illum natus nisi commodi ut optio obcaecati eius modi! Officiis, laudantium in. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Accusamus, sed?</p>
                        <button class="btn btn-warning">See More</button>
                    </div>
                </div>
                <div class="col-lg-3 col-md-6 mb-3 p-1">
                    <div class="business-card">
                        <img src="@/assets/images/lifecare.png" alt="">
                        <h2>Lifecare Medical Servies</h2>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Illum natus nisi commodi ut optio obcaecati eius modi! Officiis, laudantium in. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Accusamus, sed?</p>
                        <button class="btn btn-warning">See More</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    .our-business {
        padding: 105px 15%;
    }
    .section-header {
        text-align: center;
        padding-bottom: 30px;
    }

    .section-header>div {
        color: var(--sec-color);
    }

    .section-header h2 {
        color: var(--main-color);
        font-weight: bold;
    }

    .business-card {
        display: flex;
        flex-direction: column;
        align-items: center;
        background: #dddcdc;
        padding: 40px 5px;
        gap: 20px;
        height: 450px;
        border-radius: 5px;
        text-align: center;
        position: relative;
        transition: .3s ease;
    }

    .business-card:hover {
        background: var(--main-color);
    }

    .business-card:hover h2 {
        color: #fff;
    }

    .business img {
        width: 50%;
        height: auto;
        padding-bottom: 10px;
    }

    .business-card h2 {
        color: var(--main-color);
        font-size: 24px;
        font-weight: bold;
    }

    .business-card p {
        position: absolute;
        bottom: 20%;
        color: #000;
        padding: 0 15px;
    }

    .business-card .btn {
        position: absolute;
        bottom: 4%;
    }
</style>
