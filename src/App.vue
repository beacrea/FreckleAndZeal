<template>
  <div id="app">
    <div class="container">
      <img src="../static/logo.svg" alt="Freckle and Zeal logo" class="logo">
      <h1>{{ heading }}</h1>
      <h2>{{ subheading }}</h2>
      <ImgComp class="imgComp" before="/dist/portrait1--before.jpg" after="/dist/portrait1--after.jpg" beforeLabel="Before" afterLabel="After" caption="Example of sky painting, color grading, global lighting, slimming, skin  smoothing" />

      <h3>The camera is just the beginning.</h3>
      <p>In today's digital landscape, shooting digital RAWs can bring out the best in photos, often when the shoot itself was less-than-ideal. When photographers get back to the studio, they have hundreds of shots to pick through and hours of refinement. We help you focus on catching those perfect moments and not the development later on.</p>

      <ImgComp class="imgComp" before="/dist/portrait2--before.jpg" after="/dist/portrait2--after.jpg" beforeLabel="Before" afterLabel="After" caption="Example of color grading, global lighting, slimming, skin smoothing" />

      <h3>An extension of your craft.</h3>
      <p>Our services extend the capacity of your studio, letting you take on more projects and improve your turn-around, all without compromising the quality you're known for.</p>
    </div>
    <footer>
      <h1>Contact</h1>
    </footer>
  </div>
</template>

<script>
  // Import photo comparison component
  import ImgComp from './components/PhotoComparison';

  export default {
    components: {ImgComp},
    data () {
      return {
        heading: 'Post-processing services.',
        subheading: 'Photo-editing, manipulation, & restoration',
        imgs_beforeafter: this.importAll(require.context('../static/before_after/', false, /\.(png|jpe?g|svg)$/)),
        imgs_dir: '/dist'
      }
    },
    created: function() {

    },
    methods: {
      importAll: function (r) {
        return r.keys().map(r);
      }
    }
  }
</script>

<style lang="scss">
  // Imports
  @import "./globalStyles/global";

  #app {
    background: $color-main_light;
    margin: 0 auto;
    .container {
      padding: $common_padding $common_padding $common_padding*2;
      flex: 1 auto;
      text-align: center;
    }
    .logo {
      // local vars
      $size: 12rem;

      // styles
      height: $size;
      width: $size;
      max-width: 100%;
      margin-bottom: 1.6rem;

    }
    .imgComp {
      margin: 3.2rem 0;
    }
    footer {
      margin-top: 6.4rem;
      background: $color-brand_mainColor_base;
      padding: $common_padding;
      h1 {
        color: $color-main_light;
        text-align: center;
      }
    }
  }

  @media screen and (min-width: 76.8rem) {
    // Large Screen Rules
    #app {
      .container {
        margin: 0 auto;
        max-width: $common_siteMaxWidth;
      }
    }
  }
</style>
