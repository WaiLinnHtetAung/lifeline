<template>
    <div class="our-business">
        <v-card>
            <v-toolbar
              color="#039BE5"
            >
              <v-toolbar-title style="color: #fff; font-weight:bolder; font-size: 24px;">Our Business</v-toolbar-title>
            </v-toolbar>
            <div class="d-flex flex-row">
              <v-tabs
                v-model="tab"
                direction="vertical"
                color="#FF8C00"
                class="tab-title"
              >
                <v-tab value="option-1" class="single-tab">
                  <v-icon start style="margin-left: 10px;">
                    mdi-bag-personal
                  </v-icon>
                  Our Business
                </v-tab>
                <v-tab value="option-2" class="single-tab">
                  <v-icon start style="margin-left: 10px;">
                    <img :src="require('@/assets/images/llbg.png')" alt="">
                  </v-icon>
                    Lifeline
                </v-tab>
                <v-tab value="option-3" class="single-tab">
                  <v-icon start style="margin-left: 10px;">
                    <img :src="require('@/assets/images/mbdbg.png')" alt="">
                  </v-icon>
                  Myanmar Booster Distribution
                </v-tab>
                <v-tab value="option-4" class="single-tab">
                    <v-icon start style="margin-left: 10px;">
                      <img :src="require('@/assets/images/loyan-lifelinebg.png')" alt="">
                    </v-icon>
                    Loyal Lifeline
                  </v-tab>
                  <v-tab value="option-5" class="single-tab">
                    <v-icon start style="margin-left: 10px;">
                      <img :src="require('@/assets/images/lifecarebg.png')" alt="">
                    </v-icon>
                    Lifecare
                  </v-tab>
                </v-tabs>
              
                <v-window v-model="tab" class="tab-content-container" style="border-left: 1px solid var(--sec-color);">
                    <v-window-item value="option-1">
                    <v-card flat>
                        <div class="swiper">
                            <div class="swiper-wrapper">
                                <div class="swiper-slide">
                                    <div class="content">
                                        <img :src="require('@/assets/images/ll.png')" alt="">
                                        <router-link to="#">Lifeline</router-link>
                                    </div>
                                </div>
                                <div class="swiper-slide">
                                    <div class="content">
                                        <img class="mbd-img" :src="require('@/assets/images/mbd.png')" alt="">
                                        <router-link to="#">MBD</router-link>
                                    </div>
                                </div>
                                <div class="swiper-slide">
                                    <div class="content">
                                        <img :src="require('@/assets/images/loyan-lifeline.png')" alt="">
                                        <router-link to="#">Loyal Lifeline</router-link>
                                    </div>
                                </div>
                                <div class="swiper-slide">
                                    <div class="content">
                                        <img :src="require('@/assets/images/lifecare.png')" alt="">
                                        <router-link to="#">Lifecare</router-link>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="swiper-pagination" id="swiper-paginate"></div>
                    </v-card>
                    </v-window-item>
                    <v-window-item value="option-2">
                    <v-card flat>
                        <v-card-text class="m-3">
                            <img class="float-start float-img m-2" :src="require('@/assets/images/ll.png')" alt="">   
                            <h2>Lifeline</h2>
                            <p class="mb-0">
                                Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Velit minima facere expedita molestias assumenda doloribus, cumque ipsum adipisci praesentium, tempora aliquid suscipit autem, nostrum dolore quam eius commodi? Facere, sed veniam! Repellendus quaerat, tempore dolorem culpa, laudantium dignissimos quas sed, natus facere aperiam tenetur similique eum deleniti cumque? Porro, similique. In dui magna, posuere eget, vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis, dictum sed, iaculis a, condimentum nec, nisi.
                            </p>
                        </v-card-text>
                    </v-card>
                    </v-window-item>
                    <v-window-item value="option-3">
                    <v-card flat>
                        <v-card-text class="m-3">
                            <img class="float-start float-img m-2" :src="require('@/assets/images/mbd.png')" alt="">   
                            <h2>Myanmar Booster Distribution</h2>
                            <p class="mb-0">
                                Donec venenatis vulputate lorem. Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione maxime minima blanditiis saepe reprehenderit quo corrupti praesentium, natus vel molestiae. Aenean viverra rhoncus pede. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Velit minima facere expedita molestias assumenda doloribus, cumque ipsum adipisci praesentium, tempora aliquid suscipit autem, nostrum dolore quam eius commodi? Facere, sed veniam! Repellendus quaerat, tempore dolorem culpa, laudantium dignissimos quas sed, natus facere aperiam tenetur similique eum deleniti cumque? Porro, similique. In dui magna, posuere eget, vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis, dictum sed, iaculis a, condimentum nec, nisi.
                            </p>
                        </v-card-text>
                    </v-card>
                    </v-window-item>
                    <v-window-item value="option-4">
                        <v-card flat>
                            <v-card-text class="m-3">
                                <img class="float-start float-img m-2" :src="require('@/assets/images/loyan-lifeline.png')" alt="">   
                                <h2>Loyal Lifeline</h2>
                                <p class="mb-0">
                                    Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Velit minima facere expedita molestias assumenda doloribus, cumque ipsum adipisci praesentium, tempora aliquid suscipit autem, nostrum dolore quam eius commodi? Facere, sed veniam! Repellendus quaerat, tempore dolorem culpa, laudantium dignissimos quas sed, natus facere aperiam tenetur similique eum deleniti cumque? Porro, similique. In dui magna, posuere eget, vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis, dictum sed, iaculis a, condimentum nec, nisi.
                                </p>
                            </v-card-text>
                        </v-card>
                    </v-window-item>
                    <v-window-item value="option-5">
                        <v-card flat>
                            <v-card-text class="m-3">
                                <img class="float-start float-img m-2" :src="require('@/assets/images/lifecare.png')" alt="">   
                                <h2>Lifecare</h2>
                                <p class="mb-0">
                                    Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Velit minima facere expedita molestias assumenda doloribus, cumque ipsum adipisci praesentium, tempora aliquid suscipit autem, nostrum dolore quam eius commodi? Facere, sed veniam! Repellendus quaerat, tempore dolorem culpa, laudantium dignissimos quas sed, natus facere aperiam tenetur similique eum deleniti cumque? Porro, similique. In dui magna, posuere eget, vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis, dictum sed, iaculis a, condimentum nec, nisi.
                                </p>
                            </v-card-text>
                        </v-card>
                    </v-window-item>
                </v-window>
            </div>
        </v-card>
    </div>
</template>

<script>
import { onMounted, ref } from 'vue'
    export default {
        setup() {
            const tab = ref('option-1');
            const swiper = ref(null);

            onMounted(() => {
                swiper.value = new Swiper('.swiper', {
                    speed: 800,
                    loop: true,
                    autoplay: {
                        delay: 3000,
                        disableOnInteraction: false
                    },
                    pagination: {
                        el: '.swiper-pagination',
                        clickable: true,
                        type: 'bullets',
                    },
                    slidesPerView: 2,
                }) 
            })

            return {tab}
        }
    }
</script>

<style scoped>
    .our-business {
        padding: 40px 15%;
    }
    .swiper .swiper-wrapper {
        height: 320px;
        margin-bottom: 15px;
    }

    .swiper .swiper-slide {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .swiper-slide .content {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background: #fdf5e8;
        height: 250px;
        margin: 10px 30px;
        position: relative;
    }

    .swiper .swiper-wrapper img {
        width: 60%;
        margin-bottom: 30px;
    }

    .swiper .swiper-wrapper .mbd-img {
        width: 100%;
    }

    .swiper .swiper-slide a {
        text-decoration: none;
        background: #039BE5;
        color: #fff;
        padding: 5px 20px;
        border-radius: 7px;
        position: absolute;
        bottom: 15px;
    }

    .float-img {
        width: 200px;
    }

    .tab-content-container h2{
        font-weight: bolder;
    }

    @media (max-width: 1500px) {
        .our-business {
            padding: 40px 9%;
        }

        
        .our-business .tab-title  .single-tab {
            font-size: 13px;
        }
        .swiper .swiper-wrapper {
            height: 300px;
            margin-bottom: 15px;
        }
    
        .swiper-slide .content {
            height: 200px;
            margin: 10px 30px;
        }
    
        .swiper .swiper-wrapper img {
            width: 60%;
            margin-bottom: 30px;
        }
    
        .swiper .swiper-slide a {
            text-decoration: none;
            background: #039BE5;
            color: #fff;
            padding: 3px 20px;
            border-radius: 7px;
            position: absolute;
            bottom: 15px;
        }

        .tab-content-container h2{
            font-size: 25px;
        }
    }
</style>
