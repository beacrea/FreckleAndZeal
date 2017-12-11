<template>
  <div class="PhotoComparison">
    <h1>{{slider_title}}</h1>
    <input type="range" min="0" max="2" v-bind:value="init_value" class="slide">
    <div class="labels">
      <span>{{range1_title}}</span>
      <span>{{range2_title}}</span>
      <span>{{range3_title}}</span>
    </div>
  </div>
</template>

<script>
  // Import city model
  import cities from '../store/states'

  // Component logic
  export default {
    props: ['img1', 'img2'],
    data () {
      return {
      }
    }
  }
</script>

<style lang="scss">
  // Imports
  @import "../globalStyles/global";

  // Component Vars
  $assetsPath: '../../static/';

  // Styles
  .Slider {
    width: 100%;
  }
</style>
