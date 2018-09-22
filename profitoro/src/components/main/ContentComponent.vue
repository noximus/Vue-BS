//  ContentComponents.vue
<template>
<div>
  <promodoro-timer></promodoro-timer>
  <workouts></workouts>
  <settings></settings>
  <statistics></statistics>
</div>
</template>
<script>
import {PromodoroTimer, Settings, Statistics, Workouts} from './sections'
export default {
  components: {
    PromodoroTimer,
    Settings,
    Statistics,
    Workouts
  }
}
</script>
<style>
</style>
