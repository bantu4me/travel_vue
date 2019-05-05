<template>
  <div>
    <home-header></home-header>
    <my-swiper></my-swiper>
    <div>
      test
    </div>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import MySwiper from './components/MySwiper'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    MySwiper
  }
}
</script>

<style scoped>
</style>
