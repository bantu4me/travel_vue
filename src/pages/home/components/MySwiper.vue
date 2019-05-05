<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"/>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'MySwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: 'a0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1612/55/555b08caf0bce928a3.img.png_600x330_03ab79bf.png'
        },
        {
          id: 'a0002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1608/80/80bbeace7a29056fa3.img.jpg_600x330_1abbfcc7.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #ffffff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 55%
    background: #eee
    .swiper-img
      width: 100%
</style>
