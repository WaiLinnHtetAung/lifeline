<template>
    <div class="introduction">
        <img src="@/assets/images/introduction-banner.jpg" alt="">
        <div class="content">
            <h2>Introduction</h2>
            <div class="divider"></div>
        </div>
        <div class="para">
            <p>Lifeline Myanmar is a group of companies focusing mainly on importing, marketing and distribution of quality healthcare products for our people.</p>
            <p>Our head office is located on No.13 , 7th Hlaing Myint Moh Street, Quarter 10, Hlaing Township, Yangon, Myanmar, the close area of prime business area.</p>
        </div>
        <div class="company-img">
            <img src="@/assets/images/head-office1.jpg" alt="" class="img1">
            <img src="@/assets/images/head-office2.jpg" alt="" class="img2">
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    .introduction img {
        width: 100%;
        height: 350px;
        object-fit: cover;
    }

    .content {
        margin: 40px 0 35px;
    }

    .content h2 {
        color: var(--main-color);
        font-weight: bold;
    }
    .content .divider {
        width: 80px;
        height: 5px;
        background-color: var(--sec-color);
    }

    .para p {
        line-height: 30px;
    }

    .company-img {
        margin: 50px auto 30px;
        text-align: right;
    }

    .company-img .img1 {
        width: 60%;
        float: left;
    }

    .company-img .img2 {
        width: 50%;
        margin-top: -120px;
    }

    @media (max-width: 1600px) {
        .introduction img {
            width: 100%;
            height: 270px;
            object-fit: cover;
        }
    
        .content {
            margin: 30px 0 10px;
        }
    
        .content h2 {
            font-size: 24px;
        }
        .content .divider {
            width: 60px;
            height: 3px;
        }
    
        .para p {
            line-height: 30px;
            font-size: 14px;
        }
    
        .company-img {
            margin: 20px auto 10px;
        }
    
        .company-img .img1 {
            width: 60%;
            height: 250px;
            float: left;
        }
    
        .company-img .img2 {
            width: 50%;
            height: 250px;
            margin-top: -100px;
        }
    }

    
</style>
