<template>
    <div class="footer">
        <div class="logo">
            
            <div class="logo-img">
                <img class="lifeline" src="@/assets/images/ll.png" alt="">
                <img class="mbd" src="@/assets/images/mbd.png" alt="">
                <img class="loyallifeline" src="@/assets/images/loyan-lifeline.png" alt="">
                <img class="lifecare" src="@/assets/images/lifecare.png" alt="">
            </div>

            <h2>
                LIFELINE GROUP OF COMPANIES
            </h2>
        </div>
        <div class="row location ">
            <div class="col-lg-7">
                <div class="row mt-5">
                    <div class="col-lg-5 ">
                        <div class="row mb-3">
                            <div class="col-lg-1 ">
                                <i class="fa-solid fa-location-dot"></i>
                            </div>
                            <div class="col-lg-9 ms-3">
                                No.238, Testing St, Testing  Township, Yangon
                            </div>
                        </div>
                        <div class="row mb-3">
                            <div class="col-lg-1 ">
                                <i class="fa-solid fa-phone-volume"></i>
                            </div>
                            <div class="col-lg-9 ms-3">
                                +959 - 2343423442 <br>
                                +959 - 4432325902
                            </div>
                        </div>
                        <div class="row mb-3">
                            <div class="col-lg-1 ">
                                <i class="fa-solid fa-envelope"></i>
                            </div>
                            <div class="col-lg-9 ms-3">
                                inquiry@lifelinemyanmar.com
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-7  lifeline-link">
                        <div class="row">
                            <div class="col-lg-6">
                                <h2>About Lifeline</h2>
                                <ul>
                                    <li>Introduction</li>
                                    <li>CEO Message</li>
                                    <li>Vision & Mission</li>
                                    <li>Company MileStone (Timeline)</li>
                                    <li>CSR Activity</li>
                                    <li>News & Events</li>
                                    
                                </ul>
                            </div>
                            <div class="col-lg-6">
                                <h2>&nbsp;</h2>
                                <ul>
                                    <li>Categories</li>
                                    <li>Our Porducts</li>
                                    <li>Product Promotions</li>
                                    <li>Services & Promotions</li>
                                    <li>Principle Partners</li>
                                    <li>Hospital Partners</li>
                                    <li>Contact</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-lg-5">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d794.96138933151!2d96.13091972674002!3d16.837824966492192!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x30c1950017207cd5%3A0xe9fa12534c33c00c!2sLifeline%20Group%20of%20Companies!5e0!3m2!1sen!2smm!4v1688320014597!5m2!1sen!2smm" width="600" height="300" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
        </div>

        <hr>

        <div class="social mb-5">
            <i style="color: #3b5998;" class="fa-brands fa-facebook"></i>
            <i style="color: #8f5db7;" class="fa-brands fa-viber"></i>
            <i style="color: #CD201F;" class="fa-brands fa-youtube"></i>
            <i style="color: #0072b1" class="fa-brands fa-linkedin"></i>
        </div>
        <div class="d-flex justify-content-between align-items center">
            <div>© Copy Right Served.</div>
            <div>Lifeline Group of Companies</div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    .footer {
        padding: 30px 9% 10px;
        background-image: linear-gradient(to bottom, rgb(91, 196, 235), rgba(62, 188, 192, 0.5));
    }

    .footer .logo {
        display: flex;
        flex-direction: column;
        align-items: start;
        justify-content: center;
    }

    .footer .logo h2 {
        font-weight: bold;
        font-size: 30px;
        color: rgb(255, 255, 255);
        padding-top: 5px;
        letter-spacing: 2px;
    }
    .footer .logo img {
        object-fit: contain;
        margin-right: 40px;
    }

    .footer .lifeline {
        width: 110px;
        height: 100px;
    }

    .footer .mbd {
        width: 150px;
        height: 100px;
        object-fit: fill !important;
    }

    .footer .loyallifeline {
        width: 130px;
        height: 100px;
    }

    .footer .lifecare {
        width: 110px;
        height: 100px;
    }
    .location {
        margin-top: 10px;
    }

    .location i {
        font-size: 22px;
        color: rgb(40, 143, 184);
    }

    .location .lifeline-link h2 {
        font-size: 19px;
        font-weight: bold;
    }

    .location .lifeline-link ul li {
        list-style: none;
        margin: 0 0 5px -30px;
        font-size: 14px;
        text-decoration: underline;
    }

    .social {
        text-align: center;
    }

    .social i {
        font-size: 48px;
        margin: 5px 30px;
    }
</style>
