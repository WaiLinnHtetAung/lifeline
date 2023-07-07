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
                        <img class="lifeline" src="@/assets/images/ll.png" alt="">
                        <h2>Lifeline</h2>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Illum natus nisi commodi ut optio obcaecati eius modi! Officiis, laudantium in. Lorem ipsum dolor, sit amet consectetur a</p>
                        <button class="btn btn-warning">See More</button>
                    </div>
                </div>
                <div class="col-lg-3 col-md-6 mb-3 p-1">
                    <div class="business-card">
                        <img class="mbd" src="@/assets/images/mbd.png"  alt="">
                        <h2 class="mbd">Myanmar Booster Destribution</h2>
                        <p>Lorem, ipsum dolor sit ametnisi commodi ut optio obcaecati eius modi! Officiis, laudantium in. Lorem ipsum dolor, sit amet consectetur a</p>
                        <button class="btn btn-warning">See More</button>
                    </div>
                </div>
                <div class="col-lg-3 col-md-6 mb-3 p-1">
                    <div class="business-card">
                        <img class="loyallifeline" src="@/assets/images/loyan-lifeline.png" alt="">
                        <h2>Loyal Lifeline</h2>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Illum natus nisi commodi ut optio obcaecati eius modi! Officiis, laudantium in. Lorem ipsum dolor, sit amet consectetur a</p>
                        <button class="btn btn-warning">See More</button>
                    </div>
                </div>
                <div class="col-lg-3 col-md-6 mb-3 p-1">
                    <div class="business-card">
                        <img class="lifecare" src="@/assets/images/lifecare.png" alt="">
                        <h2>Lifecare Medical Servies</h2>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Illum natus nisi commodi ut optio obcaecati eius modi! Officiis, laudantium in. Lorem ipsum dolor, sit amet consectetur a</p>
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
        padding: 95px 15%;
    }
    .section-header {
        text-align: center;
        padding-bottom: 30px;
    }

    .section-header>div {
        color: var(--sec-color);
    }

    .section-header h2 {
        color: #fff;
        font-weight: bold;
    }

    .business-card {
        display: flex;
        flex-direction: column;
        align-items: center;
        background-image: linear-gradient(to bottom, rgb(31, 202, 214,.8), rgb(168, 122, 41));
        padding: 40px 5px;
        gap: 20px;
        height: 450px;
        border-radius: 5px;
        text-align: center;
        position: relative;
        transition: .3s ease;
    }

    .business-card:hover {
        background: #40a4ac;
    }

    .business-card:hover h2 {
        color: #fff;
    }

    .business img {
        height: 100px;
        padding-bottom: 10px;
        object-fit: contain;
    }

    .business .lifeline {
        width: 150px;
    }

    .business .mbd {
        height:180px;
        margin-top: -40px;
    }

    .business .loyallifeline {
        height: 120px;
        margin-top: -20px;
    }

    .business-card h2 {
        color: var(--main-color);
        font-size: 24px;
        font-weight: bold;
    }

    .business-card p {
        position: absolute;
        bottom: 16%;
        color: #e2dede;
        padding: 0 15px;
    }

    .business-card .btn {
        position: absolute;
        bottom: 4%;
    }
</style>
