<template>
  <div class="home">
    <Carousel></Carousel>
    <Welcome></Welcome>
    <OurBusiness></OurBusiness>
  </div>
</template>

<script>
import Welcome from '../components/Welcome'
import OurBusiness from '../components/OurBusiness'
import Carousel from '../components/Carousel'
// @ is an alias to /src

export default {
  components: {
    Welcome,
    OurBusiness, Carousel },
  name: 'HomeView',

}
</script>
