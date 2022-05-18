<template>
  <header >
    <div class="header-container">
     
      <div class="top-header">
        <div class="logo">
          <img src="../assets/images/gym_logo_1x.png" alt="">
        </div>
        <nav-bar />
        <button class="red">{{textButton.toUpperCase()}}</button>
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
  data(){
      return {
          textButton: 'Join us Today'
      }
  },
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
  // background-position-y: -50%;  da applicare a una media query sopra i 1400px
  background-size: cover;
 
}

.header-container {
  height: 100%;
  
}

.top-header {
  display: flex;
  justify-content: space-between;
  margin: 0 5% 5%;
  padding-top: 1%;
  align-items: baseline;
}

header .container {
  height: calc(100% - 133px);
  display: flex;
  flex-direction: column;
  align-items: center;
  // justify-content: center;
  // position: relative;
  // bottom: 126px;
  h1, button {
    text-transform: uppercase;
  }
}

h1 {
  font-size: 107px;
  font-weight: 700;
}
p {
  font-size: 24px;
  margin-top: 60px;
}

 button {
  background: none;
  color: $textWhite;
  border: 1px solid $textWhite;
  padding: 15px 40px;
  margin-top: 20px;
}

.red {
    padding: 30px 35px;
    background-color: $textRose1;
    color: $textWhite;
    border: 1px solid $textRose1;
    }
  

.debug {
  border: 1px solid black;
}

</style>
