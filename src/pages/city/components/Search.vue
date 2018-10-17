<template>
  <div class="search">
    <input class="search-input" type="text" name="" placeholder="请输入城市名或拼音">
  </div>
</template>

<script>
export default {
  name: 'CitySearch',
  props: {
    city: String
  }
}
</script>

<style lang="scss" scoped>
  @import '~styles/varibles.scss';
  // @import '~@/assets/varibles.scss';
  .search {
    height: .72rem;
    line-height: .72rem;
    background: $bgColor;
    text-align: center;
    padding: 0 .15rem;
    .search-input {
      // box-sizing: border-box;为元素指定的任何内边距和边框都将在已设定的宽度和高度内进行绘制。通过从已设定的宽度和高度分别减去边框和内边距才能得到内容的宽度和高度。
      box-sizing: border-box;
      width: 100%;
      text-align: center;
      height: .5rem;
      line-height: .5rem;
      border-radius: .06rem;
      padding: 0 .2rem;
    }
  }
</style>
