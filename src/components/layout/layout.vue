<template lang="pug">
.container
  .flex
    .left
    .middle
      p flex
    .right
  .table
    .left
    .middle
      p table
    .right
  .float
    .left
    .right
    .middle
      p float
  .absolute
    .left
    .middle
      p absolute
    .right
  //.five
  //  .left
  //  .middle
  //  .right
</template>

<script>
export default {
}
</script>

<style lang="sass" scoped>
.container
  > div
    margin-bottom: 10px
  div
    min-height: 60px
  .flex
    display: flex
    .left
      flex-basis: 300px
    .right
      flex-basis: 300px
    .middle
      flex: 1
  .table
    display: table
    width: 100%
    div
      display: table-cell
    .left
      width: 300px
    .right
      width: 300px
  .float
    .left
      width: 300px
      float: left
    .right
      width: 300px
      float: right
  .absolute
    position: relative
    padding-left: 20px
    margin-left: 20px
    border-left: 10px solid red
    /*margin-left: 20px*/
    div
      position: absolute
    .left
      width: 300px
      left: 0
    .right
      width: 300px
      right: 0
    .middle
      left: 300px
      right: 300px
.left
  background-color: rebeccapurple
.middle
  background-color: indianred
.right
  background-color: darkseagreen
</style>
