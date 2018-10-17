<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <icons></icons>
  </div>
</template>

<script>
import HomeHeader from '@/pages/home/components/HomeHeader'
import HomeSwiper from '@/pages/home/components/HomeSwiper'
import icons from '@/pages/home/components/icons'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    icons
  }
}
</script>
