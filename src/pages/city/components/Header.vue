<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="header-back">
        <span class="iconfont">&#xe7ea;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader',
  props: {
    city: String
  }
}
</script>

<style lang="scss" scoped>
  @import '~styles/varibles.scss';
  // @import '~@/assets/varibles.scss';
  .header {
    height: .86rem;
    line-height: .86rem;
    background: $bgColor;
    text-align: center;
    color: #fff;
    .header-back {
      position: absolute;
      width: .64rem;
      top: 0;
      left: 0;
      color: #fff;
      text-align: center;
    }
  }
</style>
