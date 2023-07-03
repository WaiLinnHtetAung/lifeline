<template>
    <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel">
        <!-- data-bs-ride="carousel" -->
        <div class="carousel-indicators">
          <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
          <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
          <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img style="filter: brightness(.5);" src="@/assets/images/head-office1.jpg" class="d-block w-100" alt="...">

            <div class="carousel-caption core-value">
                <img src="@/assets/images/core-value.png" alt="">
                <div>
                    <h3>Our Core Value</h3>
                    <ul >
                        <li>Satification</li>
                        <li>Trust</li>
                        <li>Mutual Respect</li>
                    </ul>
                    <button class="btn btn-warning ms-2">About Us</button>
                </div>
            </div>
          </div>
          <div class="carousel-item">
            <img src="@/assets/images/carousel1.jpg" class="d-block w-100" alt="...">
            <div class="carousel-caption">
                <div>
                    <div class="line"></div>
                    <img src="@/assets/images/ll.png" alt="">
                    <div class="line"></div>
                </div>
                <h3>PROTECT THE HEALTH OF YOUR ENTIRE FAMILY WITH LIFELINE</h3>
                <P>Stay Healthy, Stay Happy</P>
            </div>
            
          </div>
          <div class="carousel-item">
            <img src="@/assets/images/carousel2.png" class="d-block w-100" alt="...">
          </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    .carousel-item img {
        width: 100%;
        height: 700px;
        object-fit: cover;
        filter: brightness(.8);
    }

    .carousel-item .carousel-caption .line {
        height: 2px;
        background: #ff8c00;
        width: 100px;
    }

    .carousel-caption>div {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 15px;
    }

    .carousel-item .carousel-caption img {
        width: 90px;
        height: auto;
    }

    .carousel-caption h3 {
        margin: 20px;
        font-weight: 700;
        font-size: 35px;
    }

    .carousel-caption p {
        font-size: 18px;
        color: #6e6c6c;
    }
    .carousel-caption {
        width: 500px;
        bottom: 20%;
        left: 60%;
    }

    .carousel-caption.core-value {
        display: flex;
        align-items: center;
        width: 100%;
        gap: 150px;
        left: 30%;
        text-align: start !important;
    }

    .carousel-caption.core-value img {
        width: 350px;
    }

    .carousel-caption.core-value div {
        display: flex;
        flex-direction: column;
        gap: 20px;
        align-items: start;
        justify-content: start;
        margin-bottom: 20px;
    }

    .carousel-caption.carousel-caption.core-value ul li {
        font-size: 18px;
    }
</style>
