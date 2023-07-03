<template>
    <div class="footer">
        <div class="logo">
            <h2>
                Lifeline Group of <br> <span>Companies</span>
            </h2>
            <div class="logo-img">
                <img src="@/assets/images/ll.png" alt="">
                <img src="@/assets/images/mbd.png" alt="">
                <img src="@/assets/images/loyan-lifeline.png" alt="">
                <img src="@/assets/images/lifecare.png" alt="">
            </div>
        </div>
        <div class="row location ">
            <div class="col-lg-7">
                <div class="row mt-5">
                    <div class="col-lg-6">
                        <div class="row mb-3">
                            <div class="col-lg-1 ">
                                <i class="fa-solid fa-location-dot"></i>
                            </div>
                            <div class="col-lg-9">
                                No.238, Testing St, Testing  Township, Yangon
                            </div>
                        </div>
                        <div class="row mb-3">
                            <div class="col-lg-1 ">
                                <i class="fa-solid fa-phone-volume"></i>
                            </div>
                            <div class="col-lg-9">
                                +959 - 2343423442 <br>
                                +959 - 4432325902
                            </div>
                        </div>
                        <div class="row mb-3">
                            <div class="col-lg-1 ">
                                <i class="fa-solid fa-envelope"></i>
                            </div>
                            <div class="col-lg-9">
                                inquiry@lifelinemyanmar.com
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-6 lifeline-link">
                        <h2>About Lifeline</h2>
                        <ul>
                            <li>CEO Message</li>
                            <li>Vision & Mission</li>
                            <li>Company MileStone (Timeline)</li>
                            <li>CSR Activity</li>
                            <li>News & Events</li>
                        </ul>
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
        padding: 90px 9% 10px;
        background-image: linear-gradient(to bottom, rgb(91, 196, 235), rgb(254,138,37, .6));
    }

    .footer .logo {
        display: flex;
        align-items: center;
        gap: 90px;
    }

    .footer .logo h2 {
        font-weight: bold;
        font-size: 34px;
        color: #fff;
    }
    .footer .logo h2 span {
        letter-spacing: 10px;
    }

    .footer .logo img {
        width: 150px;
        height: auto;
        object-fit: cover;
        margin-right: 40px;
    }

    .location {
        margin-top: 50px;
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
        margin: 10px 30px;
    }
</style>
