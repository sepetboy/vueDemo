<template>
  <div class="header">
    <div class="header-back">
      <span class="iconfont">&#xe7ea;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      <span>输入城市/景点/游玩主题</span>
    </div>
    <div class="header-city">
      三亚
      <span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="scss" scoped>
  @import '~styles/varibles.scss';
  // @import '~@/assets/varibles.scss';
  .header {
    display: flex;
    height: .86rem;
    line-height: .86rem;
    background: $bgColor;
    .header-back {
      width: .64rem;
      float: left;
      color: #fff;
      text-align: center;
    }
    .header-input {
      flex: 1;
      height: .562rem;
      line-height: .56rem;
      margin-top: .15rem;
      border: 1px solid #ccc;
      border-radius: 5px;
      background: #fff;
      color: #ccc;
      text-align: left;
      text-indent: 10px;
    }
    .header-city {
      width: 1.24rem;
      float: right;
      color: #fff;
      text-align: center;
      .arrow-icon {
        font-size: .24rem;
      }
    }
  }
</style>
