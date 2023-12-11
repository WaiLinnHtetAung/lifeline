<template>
  <div class="our-business">
    <v-card>
      <v-toolbar color="#039BE5">
        <v-toolbar-title
          style="color: #fff; font-weight: bolder; font-size: 24px"
          >Our Activities</v-toolbar-title
        >
      </v-toolbar>
      <div class="d-flex flex-row">
        <v-tabs
          v-model="tab"
          direction="vertical"
          color="#FF8C00"
          class="tab-title"
        >
          <v-tab value="option-1" class="single-tab">
            <v-icon start style="margin-left: 10px"> mdi-bag-personal </v-icon>
            Our Activities
          </v-tab>
        </v-tabs>

        <v-window
          v-model="tab"
          class="tab-content-container"
          style="border-left: 1px solid var(--sec-color)"
        >
          <v-window-item value="option-1">
            <v-card flat>
              <div class="swiper">
                <div class="swiper-wrapper">
                  <div class="swiper-slide" v-for="i in 6" :key="i">
                    <div class="content">
                      <img
                        :src="require(`@/assets/images/csr/csr${i}.png`)"
                        alt=""
                      />
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
import { onMounted, ref } from "vue";
export default {
  setup() {
    const tab = ref("option-1");
    const swiper = ref(null);

    onMounted(() => {
      swiper.value = new Swiper(".swiper", {
        speed: 800,
        loop: true,
        autoplay: {
          delay: 3000,
          disableOnInteraction: false,
        },
        pagination: {
          el: ".swiper-pagination",
          clickable: true,
          type: "bullets",
        },
        breakpoints: {
          370: {
            slidesPerView: 1,
            spaceBetween: 10,
          },

          990: {
            slidesPerView: 2,
            spaceBetween: 10,
          },
        },
      });
    });

    return { tab };
  },
};
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

.swiper .swiper-wrapper img {
  width: 100%;
  height: 300px;
  object-fit: cover;
  margin: 20px auto;
}

.swiper .swiper-slide a {
  text-decoration: none;
  background: #039be5;
  color: #fff;
  padding: 5px 20px;
  border-radius: 7px;
  position: absolute;
  bottom: 15px;
}

.tab-content-container h2 {
  font-weight: bolder;
}

@media (max-width: 1600px) {
  .our-business {
    padding: 40px 9%;
  }
}

@media (max-width: 1200px) {
  .our-business {
    padding: 40px 3%;
  }

  .swiper .swiper-wrapper img {
    width: 90%;
    height: 300px;
    object-fit: cover;
    margin: 20px auto;
  }
}

@media (max-width: 990px) {
  .swiper .swiper-wrapper img {
    width: 500px;
    height: 300px;
  }
}

@media (max-width: 790px) {
  .swiper .swiper-wrapper img {
    width: 400px;
    height: 300px;
  }
}

@media (max-width: 666px) {
  .our-business .tab-title {
    display: none;
  }
  .swiper .swiper-wrapper img {
    width: 450px;
    height: 300px;
  }
}

@media (max-width: 510px) {
  .swiper .swiper-slide .content {
    padding: 0px 10px;
  }
  .swiper .swiper-wrapper img {
    width: 100%;
    height: 300px;
  }
}
</style>
