<template>
  <div>
    <home-header></home-header>
    <my-swiper></my-swiper>
    <my-icons></my-icons>
    <my-recommend></my-recommend>
    <my-weekend></my-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import MySwiper from './components/MySwiper'
import MyIcons from './components/MyIcons'
import MyRecommend from './components/MyRecommend'
import MyWeekend from './components/MyWeekend'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    MySwiper,
    MyIcons,
    MyRecommend,
    MyWeekend
  }
}
</script>

<style scoped>
</style>
