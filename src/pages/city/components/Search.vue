<template>
  <div class="search">
    <input type="text" placeholder="输入城市名或拼音" class="search-input">
  </div>
</template>
<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.search
  height: 0.722rem
  background: $bgColor
  padding: 0 0.1rem
  .search-input
    height: 0.62rem
    line-height: 0.62rem
    width: 100%
    text-align: center
    padding: 0 0.1rem
    box-sizing: border-box
    border-radius: 0.06rem
    color: #666
</style>
