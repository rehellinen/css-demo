<template lang="pug">
  div
    switch-tab(:tabs="tabs")
      div(slot="0")
        float
      div(slot="1")
        layout
</template>

<script>
import SwitchTab from './base/switch-tab/switch-tab'
import Float from './components/float/float'
import Layout from './components/layout/layout'


export default {
  components: {
    SwitchTab,
    Float,
    Layout
  },
  data () {
    return {
      tabs: ['布局', 'float']
    }
  }
}
</script>

<style lang="sass" rel="stylesheet/sass">
  .note
    margin-bottom: 10px
    margin-left: 15px
    color: #6c6c6c
</style>
