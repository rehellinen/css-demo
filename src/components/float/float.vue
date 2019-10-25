<template lang="pug">
  div
    //.note
      p float的初衷只是为了实现文字环绕效果
    //.note
      p 包裹性
      p 若内部有float:left元素，外部容器宽度为100%，高度会塌陷
      p 但是当外部容器使用了float:left的时候
      p 就会产生收缩（水平）、坚挺（垂直）、隔绝的效果，这种效果称为包裹性
      p 其他有包裹性的属性：
      p (1) display: inline-block / table-cell
      p (2) position: absolute / fixed / sticky
      p (3) overflow: hidden / scroll
    //.note
      p 破坏性
      p 其他有破坏性的属性：
      p (1) display: none
      p (2) position: absolute / fixed / sticky
    //.note
      p block化
      p 去空格化
    p.note 这里实现了文字环绕效果
    div.text-around
      img(src="../../assets/demo.jpg")
      p 文字环绕效果，文字环绕效果，文字环绕效果，文字环绕效果
    p.note 图片设置了浮动，父元素高度塌陷
    .wrapper-bfc
      .img-float
        img(src="../../assets/demo.jpg")
    p.note 使用生成BFC的方法清除浮动
    .wrapper-bfc
      img(src="../../assets/demo.jpg")
    p.note 使用clear属性清除浮动
    .wrapper-clear.clear-fake
      img.clear-fake(src="../../assets/demo.jpg")
      .clear
    p.note 最简单的两栏布局
    .bfc.mb-20
      div.left-right-one
        div.left
          p 这是左边的div
          p 这是左边的div
          p 这是左边的div
          p 这是左边的div
          p 这是左边的div
        div.right
          p 这是右边的div
          p 这是右边的div
          p 这是右边的div
    p.note float + margin
    .bfc.mb-20
      div.left-right-two
        div.left
          p 这是左边的div
          p 这是左边的div
          p 这是左边的div
          p 这是左边的div
          p 这是左边的div
          p 这是左边的div
          p 这是左边的div
          p 这是左边的div
          p 这是左边的div
        div.right
          p 这是右边的div
          p 这是右边的div
          p 这是右边的div
          p 这是右边的div
          p 这是右边的div
    p.note float + BFC
    div.left-right-bfc.mb-20
      div.left
        p 这是左边的div
        p 这是左边的div
        p 这是左边的div
      div.right
        p 这是右边的div
        p 这是右边的div
        p 这是右边的div
        p 这是右边的div
        p 这是右边的div
    p.note 最简单的三栏布局
    div.left-middle-right.mb-20
      div.left
        p 这是左边的div
        p 这是左边的div
        p 这是左边的div
      div.middle
        p 这是中间的div
        p 这是中间的div
        p 这是中间的div
      div.right
        p 这是右边的div
        p 这是右边的div
        p 这是右边的div
</template>

<script>
export default {
}
</script>

<style lang="sass" scoped>
  .text-around
    width: 130px
    img
      float: left
      width: 70px
    p
      background-color: lightblue
  .img-float
    background-color: lightblue
    img
      float: left
      width: 200px
  .wrapper-bfc
    overflow: hidden
    img
      float: left
      width: 200px
  .wrapper-clear
    img
      float: left
      width: 200px
    .clear
      clear: both
    .clear-fake
      &:after
        content: ''
        display: block
        height: 0
        overflow: hidden
        clear: both
  .left
    background-color: lightblue
  .right
    background-color: palevioletred
  .middle
    background-color: lightyellow
  .left-right-one
    .left
      float: left
  .left-right-two
    .left
      float: left
    .right
      margin-left: 120px
  .left-right-bfc
    .left
      float: left
    .right
      overflow: hidden
  .left-middle-right
    .left
      float: left
    .middle
      float: left
  .de
</style>
