<template>
  <div class="home">
    <Carousel></Carousel>
    <Welcome></Welcome>
    <OurBusiness></OurBusiness>
    <!-- <Category></Category>
    <CeoMessage></CeoMessage>
    <Promotion></Promotion>
    <LatestProducts></LatestProducts>
    <OurProducts></OurProducts>
    <CompanyInfo></CompanyInfo>
    <News></News> -->
  </div>
</template>

<script>
import Welcome from '../components/Welcome'
import News from '../components/News'
import CompanyInfo from '../components/CompanyInfo'
import OurProducts from '../components/OurProducts'
import LatestProducts from '../components/LatestProducts'
import Promotion from '../components/Promotion'
import Category from '../components/Category'
import CeoMessage from '../components/CeoMessage'
import OurBusiness from '../components/OurBusiness'
import Carousel from '../components/Carousel'
// @ is an alias to /src

export default {
  components: {
    Welcome,
    News,
    CompanyInfo,
    OurProducts,
    LatestProducts,
    Promotion,
    Category,
    CeoMessage,
    OurBusiness, Carousel },
  name: 'HomeView',

}
</script>
