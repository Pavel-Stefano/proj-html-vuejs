<template>
  <header >
    <div class="header-container">
     
      <div class="top-header">
        <div class="logo">
          <img src="../assets/images/gym_logo_1x.png" alt="">
        </div>
        <nav-bar />
      </div>

      <div class="container text-center">
        <h1>No pain no gain</h1>
        <p>Motivation is what gets you started. Habit is what keeps you going.</p>
        <button>Join us today</button>
      </div>
      
    </div>

  </header>
  
</template>

<script>
import NavBar from './NavBar.vue'


export default {
  components: { 
    NavBar,

    },
  name: 'AppHeader',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/vars.scss';

header {
  background: $backgroundBlack;
  // background-blend-mode: color-dodge;  effetto sfondo più bello
  height: 100vh;
  color: $textWhite;
  background-image: url('../assets/images/home-banner.jpg');
  background-repeat: no-repeat;
  background-position: top;
 
}

.header-container {
  height: 100%;
  
}

.top-header {
  display: flex;
  justify-content: space-between;
  margin: 0 135px;
  padding-top: 90px;
  align-items: baseline;
}

header .container {
  height: calc(100% - 133px);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  position: relative;
  bottom: 93px;
  h1, button {
    text-transform: uppercase;
  }
}

h1 {
  font-size: 115px;
  font-weight: 700;
}
p {
  font-size: 24px;
}

 button {
  background: none;
  color: $textWhite;
  border: 1px solid $textWhite;
  padding: 10px 25px;
}

  

.debug {
  border: 1px solid black;
}

</style>
