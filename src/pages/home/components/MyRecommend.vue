<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item" v-for="item in recommendList" :key="item.id">
        <img class="item-img"
             :src="item.imgUrl"/>
        <div class="item-info border-bottom">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'MyRecommend',
  data () {
    return {
      recommendList: [
        {
          id: '1',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1904/1e/1e51b5ea32ee8033a3.water.jpg_200x200_7750aa0b.jpg',
          title: '梵净山',
          desc: '国家5A级风景名胜区'
        }, {
          id: '2',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1904/1e/1e51b5ea32ee8033a3.water.jpg_200x200_7750aa0b.jpg',
          title: '梵净山',
          desc: '国家5A级风景名胜区'
        }, {
          id: '3',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1904/1e/1e51b5ea32ee8033a3.water.jpg_200x200_7750aa0b.jpg',
          title: '梵净山',
          desc: '国家5A级风景名胜区'
        }, {
          id: '4',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1904/1e/1e51b5ea32ee8033a3.water.jpg_200x200_7750aa0b.jpg',
          title: '梵净山',
          desc: '国家5A级风景名胜区'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem

  .item
    overflow: hidden
    display: flex
    height: 1.9rem

    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem

    .item-info
      flex: 1
      padding: .1rem
      min-width: 0

      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()

      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()

      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
