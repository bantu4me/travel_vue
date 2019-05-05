<template>
  <div>
    <home-header></home-header>
    <my-swiper :list="swiperList"></my-swiper>
    <my-icons :list="iconList"></my-icons>
    <my-recommend :list="recommendList"></my-recommend>
    <my-weekend :list="weekendList"></my-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import MySwiper from './components/MySwiper'
import MyIcons from './components/MyIcons'
import MyRecommend from './components/MyRecommend'
import MyWeekend from './components/MyWeekend'
import axios from 'axios'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    MySwiper,
    MyIcons,
    MyRecommend,
    MyWeekend
  },
  data () {
    return {
      swiperList: [],
      iconList: [],
      recommendList: [],
      weekendList: []
    }
  },
  mounted () {
    this.getHomeInfo()
  },
  methods: {
    getHomeInfo () {
      axios.get('/static/mock/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        console.log(data)
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.weekendList = data.weekendList
      }
    }
  }
}
</script>

<style scoped>
</style>
