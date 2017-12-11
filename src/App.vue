<template>
  <div id="app">
    <div class="container">
      <img src="../static/logo.svg" alt="Freckle and Zeal logo" class="logo">
      <h1>{{ heading }}</h1>
      <h2>{{ subheading }}</h2>
      <p>Give attitude plan steps for world domination so lick the other cats. Sleep nap stretch, forpooping rainbow while flying in a toasted bread costume in space, my left donut is missing, as is my right so purr while eating, yet groom yourself 4 hours - checked, have your beauty sleep 18 hours - checked, be fabulous for the rest of the day - checked!. Groom yourself 4 hours - checked, have your beauty sleep 18 hours - checked, be fabulous for the rest of the day - checked! pelt around the house and up and down stairs chasing phantoms so find something else more interesting, so put toy mouse in food bowl run out of litter box at full speed.</p>
      <p>Ignore the squirrels, you'll never catch them anyway attack feet, for always hungry scamper, andmake meme, make cute face inspect anything brought into the house. Attack feet stare out the window hide at bottom of staircase to trip human put toy mouse in food bowl run out of litter box at full speed . My left donut is missing, as is my right kitty power! . Need to chase tail. Intently sniff hand kitty scratches couch bad kitty yet stare at ceiling, chew iPad power cord, for peer out window, chatter at birds, lure them to mouth so scratch the box. Chase dog then run away i like big cats and i can not lie paw at beetle and eat it before it gets away yet have secret plans.Unwrap toilet paper drink water out of the faucet. Damn that dog chew iPad power cord, andhowl uncontrollably for no reason.</p>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'app',
    data () {
      return {
        heading: 'Hello there!',
        subheading: 'Welcome to our super cool website'
      }
    }
  }
</script>

<style lang="scss">
  // Imports
  @import "./globalStyles/global";

  #app {
    height: 100%;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    .container {
      max-width: 60rem;
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
</style>
