<template>
    <div class="news">
        <div class="header-container mb-5">
            <div class="header">
                <div class="title">News</div>
                <div class="all">All News <i class="fa-solid fa-arrow-up"></i></div>
            </div>
            <div class="underline">

            </div>
        </div>

        <div class="news-container">
            <div class="row">
                <div class="col-lg-7">
                    <div class="row">
                        <div class="col-lg-6 large-news">
                            <img src="@/assets/images/news1.jpg" alt="">
                            <div class="news-content">
                                <h2>This article is intended for those who love to read news and blogs.</h2>
                                <div class="date">
                                    <i class="fa-solid fa-calendar"></i>
                                    <span>22-03-2023</span>
                                </div>
                                <p>This website is intended exclusively for Medicare providers and health care industry professionals to find the latest Medicare news and information affecting</p>
                                <router-link to="#" class="btn btn-outline-primary">Read More</router-link>
                            </div>
                        </div>
                        <div class="col-lg-6 large-news">
                            <img src="@/assets/images/news2.jpg" alt="">
                            <div class="news-content">
                                <h2>This article is intended for those who love to read news and blogs.</h2>
                                <div class="date">
                                    <i class="fa-solid fa-calendar"></i>
                                    <span>22-03-2023</span>
                                </div>
                                <p>This website is intended exclusively for Medicare providers and health care industry professionals to find the latest Medicare news and information affecting</p>
                                <router-link to="#" class="btn btn-outline-primary">Read More</router-link>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-lg-5 ">
                    <div class="row short-news">
                        <div class="col-lg-4 p-0">
                            <img src="@/assets/images/news1.jpg" alt="">
                        </div>
                        <div class="col-lg-8 short-news-content">
                            <div>
                                <h2>This article is intended for those who love to read news and blogs.</h2>
                                <div class="date mb-2">
                                    <i class="fa-solid fa-calendar"></i>
                                    <span>22-03-2023</span>
                                </div>
                                <router-link to="#" class="btn btn-sm btn-outline-primary">Read</router-link>
                            </div>
                        </div>
                    </div>
                    <div class="row short-news">
                        <div class="col-lg-4 p-0">
                            <img src="@/assets/images/news1.jpg" alt="">
                        </div>
                        <div class="col-lg-8 short-news-content">
                            <div>
                                <h2>This article is intended for those who love to read news and blogs.</h2>
                                <div class="date mb-2">
                                    <i class="fa-solid fa-calendar"></i>
                                    <span>22-03-2023</span>
                                </div>
                                <router-link to="#" class="btn btn-sm btn-outline-primary">Read</router-link>
                            </div>
                        </div>
                    </div>
                    <div class="row short-news">
                        <div class="col-lg-4 p-0">
                            <img src="@/assets/images/news1.jpg" alt="">
                        </div>
                        <div class="col-lg-8 short-news-content">
                            <div>
                                <h2>This article is intended for those who love to read news and blogs.</h2>
                                <div class="date mb-2">
                                    <i class="fa-solid fa-calendar"></i>
                                    <span>22-03-2023</span>
                                </div>
                                <router-link to="#" class="btn btn-sm btn-outline-primary">Read</router-link>
                            </div>
                        </div>
                    </div>
                    <div class="row short-news">
                        <div class="col-lg-4 p-0">
                            <img src="@/assets/images/news1.jpg" alt="">
                        </div>
                        <div class="col-lg-8 short-news-content">
                            <div>
                                <h2>This article is intended for those who love to read news and blogs.</h2>
                                <div class="date mb-2">
                                    <i class="fa-solid fa-calendar"></i>
                                    <span>22-03-2023</span>
                                </div>
                                <router-link to="#" class="btn btn-sm btn-outline-primary">Read</router-link>
                            </div>
                        </div>
                    </div>
                    <div class="row short-news">
                        <div class="col-lg-4 p-0">
                            <img src="@/assets/images/news1.jpg" alt="">
                        </div>
                        <div class="col-lg-8 short-news-content">
                            <div>
                                <h2>This article is intended for those who love to read news and blogs.</h2>
                                <div class="date mb-2">
                                    <i class="fa-solid fa-calendar"></i>
                                    <span>22-03-2023</span>
                                </div>
                                <router-link to="#" class="btn btn-sm btn-outline-primary">Read</router-link>
                            </div>
                        </div>
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
    .news {
        padding: 80px 15%;
    }

    .news-container img {
        width: 100%;
        height: 300px;
        object-fit: cover;
    }

    .large-news {
        height: 600px;
    }

    .news-content h2 {
        font-size: 24px;
        padding: 5px 10px 5px 5px;
        color: var(--main-color);
        font-weight: bold;
    }

    .news-content .date {
        margin: 10px auto;
    }
    .news-content i {
        color: var(--sec-color);
        margin-right: 10px;
    }

    .news-content span {
        font-weight: bold;
    }

    .news-content p {
        color: rgb(99, 102, 104);
    }

    .short-news {
        height: 120px;
    }

    .short-news img {
        width: 100%;
        height: 100%;
        height: auto;
    }

    .short-news-content {
        padding-left: 10px;
    }

    .short-news-content h2 {
        font-size: 16px;
        font-weight: bold;
    }

    .short-news-content .date i {
        color: var(--sec-color);
        margin-right: 15px;
    }
    .short-news-content .date span {
        font-weight: bold;
    }

</style>
