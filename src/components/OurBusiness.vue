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
                  Our Activities
                </v-tab>
              
                </v-tabs>
              
                <v-window v-model="tab" class="tab-content-container" style="border-left: 1px solid var(--sec-color);">
                    <v-window-item value="option-1">
                    <v-card flat>
                        <div class="swiper">
                            <div class="swiper-wrapper">
                                <div class="swiper-slide" v-for="i in 6" :key="i">
                                    <div class="content">
                                        <img :src="require(`@/assets/images/csr/csr${i}.png`)" alt="">
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="swiper-pagination" id="swiper-paginate"></div>
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
        height: 370px;
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
        height: 250px;
        margin: 10px 30px;
        position: relative;
        padding: 30px 10px;
    }

    .swiper .swiper-wrapper img {
        width: 500px;
        height: 300px;
        object-fit: cover;
        margin: 20px auto;
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

    .tab-content-container a {
        text-decoration: none;
        color: #fff;
        background: var(--sec-color);
        padding: 5px 15px;
        border-radius: 5px;
    }

    @media (max-width: 1600px) {
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

    @media (max-width: 1200px) {
        .our-business {
            padding: 40px 3%;
        }
    }
</style>
