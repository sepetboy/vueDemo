<template>
  <div>
    <home-header></home-header>
    <home-swiper :swiperList="swiperList"></home-swiper>
    <icons :iconList="iconList"></icons>
    <recommend :recommendList="recommendList"></recommend>
    <weekend :weekendList="weekendList"></weekend>
  </div>
</template>

<script>
import HomeHeader from './components/HomeHeader'
import HomeSwiper from './components/HomeSwiper'
import icons from './components/icons'
import recommend from './components/recommend'
import weekend from './components/weekend'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    icons,
    recommend,
    weekend
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
    var self = this
    this.$remote.get('static/mock/index.json')
      .then(function (response) {
        self.swiperList = response.data.data.swiperList
        self.iconList = response.data.data.iconList
        self.recommendList = response.data.data.recommendList
        self.weekendList = response.data.data.weekendList
      })
  }
}
</script>
