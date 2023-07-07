<template>
  <Navbar />
  <router-view/>
  <Footer />
</template>

<script>
  import Navbar from '@/components/Navbar.vue'
  import Footer from '@/components/Footer.vue'
  export default {
    components: {Navbar, Footer}
  }
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-image: linear-gradient(to bottom, rgb(58, 186, 218), rgba(143, 96, 25));

}

</style>
