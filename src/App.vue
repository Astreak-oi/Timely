<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->

  <BannerView />
  <HeaderView />
  <DetailsAdd msg="Welcome to Your Vue.js App" />


</template>

<script>
import DetailsAdd from './components/DetailsAdd.vue';
import HeaderView from './components/HeaderView.vue';
import BannerView from './components/BannerView.vue';

export default {
  name: 'App',
  components: {
    
    BannerView,
    HeaderView,
    DetailsAdd,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
