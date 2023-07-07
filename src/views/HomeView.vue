<template>
  <div class="home">
    <Carousel></Carousel>
    <CeoMessage></CeoMessage>
    <OurBusiness></OurBusiness>
    <!-- <Category></Category>
    <Promotion></Promotion>
    <LatestProducts></LatestProducts>
    <OurProducts></OurProducts>
    <CompanyInfo></CompanyInfo>
    <News></News> -->
  </div>
</template>

<script>
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
