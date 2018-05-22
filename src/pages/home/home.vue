<template>
  <div>
    <div class="home">
      <home-header></home-header>
    </div>
  </div>

</template>
<script>
  import HomeHeader from './components/Header.vue'
  export default {
    name:'home',
    components:{
      HomeHeader:HomeHeader
    }
  }
</script>
<style>

</style>
