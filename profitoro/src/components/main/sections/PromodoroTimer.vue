//  PromodoroTimer.vue
<template>
  <div>PromodoroTimer
    <svg-circle-sector :angle="60" :text="'hello'"></svg-circle-sector>
  </div>
</template>
<script>
import {SvgCircleSector} from './timer'
export default {
  components: {
    SvgCircleSector
  }
}
</script>
<style>
</style>
