<template lang="pug">
  switch-tab(:tabs="tabs")
    div(slot="0")
      float
    div(slot="1")
      layout
    div(slot="2")
      b-f-c
    div(slot="3")
      absolute
</template>

<script>
import SwitchTab from './base/switch-tab/switch-tab'
import Float from './components/float/float'
import Layout from './components/layout/layout'
import BFC from './components/bfc/bfc'
import Absolute from './components/absolute/absolute'


export default {
  components: {
    SwitchTab,
    Float,
    Layout,
    BFC,
    Absolute
  },
  data () {
    return {
      tabs: ['float', 'layout', 'bfc', 'absolute']
    }
  }
}
</script>

<style lang="sass" rel="stylesheet/sass">
  .bfc
    overflow: hidden
  .mb-20
    margin-bottom: 20px
  .note
    margin: 10px 10px
    color: #2c2c2c
</style>
