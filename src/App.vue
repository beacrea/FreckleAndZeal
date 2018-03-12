<template>
  <div id="app">
    <div class="container">
      <img src="../static/logo.svg" alt="Freckle and Zeal logo" class="logo">
      <h1>Post-processing services.</h1>
      <h2>Photo-editing, manipulation, & restoration</h2>
      <ImgComp class="imgComp" before="/dist/portrait1--before.jpg" after="/dist/portrait1--after.jpg" beforeLabel="Before" afterLabel="After" caption="Example of sky painting, color grading, global lighting, slimming, & skin smoothing" />

      <h3>Your camera is just a beginning.</h3>
      <p>Shooting digital RAWs can bring out the best in photos, even when the shoot itself was less-than-ideal. When photographers get back to the studio, they have hundreds of shots to pick through and hours of refinement. We help you focus on catching those perfect moments and not the development later on.</p>

      <ImgComp class="imgComp" before="/dist/portrait3--before.jpg" after="/dist/portrait3--after.jpg" beforeLabel="Before" afterLabel="After" caption="Example of color grading, global lighting, slimming, & skin smoothing" />

      <h3>An extension of your craft.</h3>
      <p>Our services extend the capacity of your studio, letting you take on more projects and improve your turn-around, all without compromising quality.</p>

      <h3>Not a photographer, but need help?</h3>
      <p>We offer private services as well for individuals.</p>
      <ul>
        <li>Family photo manipulation</li>
        <li>Historically distressed photos</li>
        <li>Wedding photography improvements</li>
        <li>And more!</li>
      </ul>
      <p class="cta_prompt">Contact us  below for more information.</p>
    </div>
    <a class="footer" :href="contactEmail" target="_blank">
      <h1>Click to Contact Us</h1>
      <p>We service clients all over the world, but have a particular soft spot for those in Kansas City and San Francisco &#10084;.</p>
    </a>
  </div>
</template>

<script>
  // Import photo comparison component
  import ImgComp from './components/PhotoComparison';

  export default {
    components: {ImgComp},
    data () {
      return {
        contactEmail: 'emaildomain'
      }
    },
    mounted: function() {
      this.contactEmail = 'mailto:' + 'hello@freckleandzeal.com'
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
    .footer {
      display: block;
      margin-top: 6.4rem;
      background: $color-brand_mainColor_base;
      padding: $common_padding*2 $common_padding;
      text-align: center;
      cursor: pointer;
      transition: all 0.5s;
      &:hover {
        background: darken($color-brand_mainColor_base, 10%);
      }
      h1 {
        color: $color-main_light;
        text-align: center;
        line-height: 1;
        margin-bottom: 0;
        font-size: 4.5rem;
      }
      p {
        color: rgba(white, 0.8);
      }
    }
    .cta_prompt {
      margin-top: 1rem;
      font-size: 2rem;
      color: $color-brand_mainColor_base;
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
