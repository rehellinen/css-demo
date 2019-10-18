<template lang="pug">
div
  p.note margin重叠：属于同一BFC的相邻block元素的竖直距离的margin会发生重叠的情况
  p.note 解决办法：生成新的bfc
  p.note 下面是兄弟元素的margin重叠问题
  .brother-margin
    .margin
    .margin
    div.bfc
      .margin
  p.note 父子元素
  .father-son-margin
    .son
  p.note 父子元素解决方案：令子元素属于另一个bfc
  .father-son-margin.bfc
    .son
  p.note 空元素的
  .empty
  p.note 空元素的
</template>

<script>
export default {

}
</script>

<style lang="sass" scoped>
  .bfc
    overflow: hidden
  .brother-margin
    .margin
      height: 10px
      margin: 10px
      background-color: lightblue
  .father-son-margin
    background-color: palevioletred
    margin-top: 10px
    .son
      background-color: yellowgreen
      height: 10px
      margin-top: 10px
  .empty
    margin-top: 30px
    margin-bottom: 40px
  .de
</style>
