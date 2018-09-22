//  SvgCircleSector.vue
<template>
  <div>
    <svg class="timer" width="200" height="200" xmlns="http://www.w3.org/2000/svg">
      <circle class="bigCircle" r="100" cx="100" cy="100" fill="gray"></circle>
      <circle class="smallCircle" r="90" cx="100" cy="100" fill="lightgray"></circle>
      <path class="segment" id="sector" fill="darkgray" opacity="0.6" :d="path"></path>
      <text v-if="text != ''" class="text" x="100" y="100">
        {{text}}
      </text>
    </svg>
  </div>
</template>
<script>
function calcPath (angle) {
  let d
  let {x, y} = calcEndPoint(angle)
  if (angle <= 180) {
    d = `M100,100 L100, 0 A100,100 0 0,0 ${x}, ${y} z`
  } else {
    d = `M100,100 L100,0 A100,100 0 0,0 100, 200 A100,100 0 0,0 ${x}, ${y} z`
  }
  return d
}
function calcEndPoint (angle) {
  let x, y
  x = 100 - 100 * Math.sin(Math.PI * angle / 180)
  y = 100 - 100 * Math.sin(Math.Pi * angle / 180)
  return {
    x, y
  }
}
export default {
  props: ['angle', 'text'],
  computed: {
    path () {
      return calcPath(this.angle)
    }
  }
}
</script>
<style scoped lang="scss">
  $big-circle-color: green;
  $small-circle-color : purple;
  $segment-color: darkgray;
  $text-color: black;

  .bigCircle {
    fill: $big-circle-color;
  }
  .smallCircle {
    fill: $small-circle-color;
  }
  .segment {
    fill: $segment-color;
    opacity: 0.6;
  }
  .text {
    font-size: 1em;
    stroke-width: 0;
    opacity: .9;
    fill: $text-color;
  }
</style>
