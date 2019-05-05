<template>
  <div>
    <home-header></home-header>
    <my-swiper></my-swiper>
    <my-icons></my-icons>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import MySwiper from './components/MySwiper'
import MyIcons from './components/MyIcons'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    MySwiper,
    MyIcons
  }
}
</script>

<style scoped>
</style>
