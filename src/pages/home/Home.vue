<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
  </div>
</template>

<script>
import HomeHeader from '@/pages/home/components/HomeHeader'
import HomeSwiper from '@/pages/home/components/HomeSwiper'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper
  }
}
</script>
