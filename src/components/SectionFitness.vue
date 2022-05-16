<template>
    <section class="fitness text-center">

        <h2>{{title.toUpperCase() + ' ' + 'Fitness'}}</h2>
        <img src="../assets/images/divider-xx-red.png" alt="">
        <p>At Avada Gym, everything we do from top to bottom is of the highest quality to ensure we're equipped <br>
        to help you reach your goals of a healthy and lifestyle.</p>
    </section>
   

</template>

<script>
export default {
  name: 'SectionFitness',
  data(){
      return {
          title: 'Word class',
      }
  },
//   props: {
//     msg: String
//   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/vars.scss';

.fitness {
    background-color: #252a2d;
    height: 400px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    color: $textWhite;
    img {
        padding: 35px 0;
    }
    h2 {
        font-size: 40px;
        font-weight: 900;
    }
    p {
        font-size: 20px;
    }
}

  
</style>