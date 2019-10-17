<template lang="pug">
  div
    .note
      p float的初衷只是为了实现文字环绕效果
    .note
      p 包裹性（其实就是BFC）
      p 若内部有float:left元素，外部容器宽度为100%，高度会塌陷
      p 但是当外部容器使用了float:left的时候
      p 就会产生收缩（水平）、坚挺（垂直）、隔绝的效果，这种效果称为包裹性
      p 其他有包裹性的属性：
      p (1) display: inline-block / table-cell
      p (2) position: absolute / fixed / sticky
      p (3) overflow: hidden / scroll
    .note
      p 破坏性
      p 其他有破坏性的属性：
      p (1) display: none
      p (2) position: absolute / fixed / sticky
    .note
      p block化
      p 去空格化
    .note
      p 图1 - 正常情况
    .note
      p 图2 - 破坏性
      p img使用了float，而容器没有使用
      p 容器宽度为100%，高度为0
    .note
      p 图3 - 包裹性
      p img和容器都使用了float
      p 容器宽度和高度都跟图片大小一样
    div.text-around
      img(src="../../assets/timg.jpg")
      p 文字环绕效果
      p 文字环绕效果
      p 文字环绕效果
      p 文字环绕效果
      p 文字环绕效果
      p 文字环绕效果
      p 文字环绕效果
      p 文字环绕效果
      p 文字环绕效果

    //.img-float
      img(src="../../assets/timg.jpg")
    //.wrapper-float
      img(src="../../assets/timg.jpg")
</template>

<script>
export default {
}
</script>

<style lang="sass" scoped>
  .text-around
    &::after
      content: ''
      display: block
      clear: both
      height: 0
      overflow: hidden
    img
      float: left
      width: 70px
  .img-float
    float: left
    img
      float: left
      width: 200px
  .wrapper-float
    position: absolute
    img
      float: left
      width: 200px
  .de
</style>
