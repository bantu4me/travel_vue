<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list :hotCities="hotCities" :cities="cities"></city-list>
    <city-alpha-beta :cities="cities"></city-alpha-beta>
  </div>
</template>

<script>
import CityHeader from './components/Header'
import CitySearch from './components/Search'
import CityList from './components/List'
import CityAlphaBeta from './components/AlphaBeta'
import axios from 'axios'

export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphaBeta
  },
  data () {
    return {
      cities: {},
      hotCities: []
    }
  },
  methods: {
    getCityInfoSucc (res) {
      res = res.data
      console.log(res)
      if (res.ret && res.data) {
        const data = res.data
        this.cities = data.cities
        this.hotCities = data.hotCities
      }
    }
  },
  mounted () {
    axios.get('/static/mock/city.json')
      .then(this.getCityInfoSucc)
  }
}
</script>

<style lang="stylus" scoped>

</style>
