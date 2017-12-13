<template>
  <div id="app">
    <div class="container">
      <img src="../static/logo.svg" alt="Freckle and Zeal logo" class="logo">
      <h1>{{ heading }}</h1>
      <h2>{{ subheading }}</h2>
      <ImgComp before="/dist/portrait1--before.jpg" after="/dist/portrait1--after.jpg" beforeLabel="Before" afterLabel="After" />
      <p>Give attitude plan steps for world domination so lick the other cats. Sleep nap stretch, forpooping rainbow while flying in a toasted bread costume in space, my left donut is missing, as is my right so purr while eating, yet groom yourself 4 hours - checked, have your beauty sleep 18 hours - checked, be fabulous for the rest of the day - checked!</p>
      <ImgComp before="/dist/portrait2--before.jpg" after="/dist/portrait2--after.jpg" beforeLabel="Before" afterLabel="After" />

      <p>Give attitude plan steps for world domination so lick the other cats. Sleep nap stretch, forpooping rainbow while flying in a toasted bread costume in space, my left donut is missing, as is my right so purr while eating, yet groom yourself 4 hours - checked, have your beauty sleep 18 hours - checked, be fabulous for the rest of the day - checked!</p>

      <p>Give attitude plan steps for world domination so lick the other cats. Sleep nap stretch, forpooping rainbow while flying in a toasted bread costume in space, my left donut is missing, as is my right so purr while eating, yet groom yourself 4 hours - checked, have your beauty sleep 18 hours - checked, be fabulous for the rest of the day - checked!</p>
    </div>
  </div>
</template>

<script>
  // Import photo comparison component
  import ImgComp from './components/PhotoComparison';

  export default {
    components: {ImgComp},
    data () {
      return {
        heading: 'Hello there!',
        subheading: 'Welcome to our super cool website',
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
    .container {
      padding: 2.4rem 2.4rem 4.8rem;
      flex: 1 auto;
      text-align: center;
      p {
        text-align: left;
      }
    }
    .logo {
      $size: 12rem;
      height: $size;
      width: $size;
      max-width: 100%;
    }
  }

  @media screen and (min-width: 76.8rem) {
    // Large Screen Rules
    #app {
      .container {
        margin: 0 auto;
        max-width: 60rem;
      }
    }
  }
</style>
