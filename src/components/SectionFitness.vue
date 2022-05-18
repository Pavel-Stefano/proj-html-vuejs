<template>
    <section class="fitness text-center">

        <h2>{{title.toUpperCase() + ' ' + 'Fitness'}}</h2>
        <img src="../assets/images/divider-xx-red.png" alt="">
        <p>At Avada Gym, everything we do from top to bottom is of the highest quality to ensure we're equipped <br>
        to help you reach your goals of a healthy and lifestyle.</p>
        <i class="fa-solid fa-square-full"></i>
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
    background-color: $backgroundGrey1;
    height: 400px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    color: $textWhite;
    position: relative;
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

i {
    color: $backgroundGrey1;
    position: absolute;
    bottom: -26px;
    transform: rotate(45deg);
    font-size: 50px;
    border: 1px solid $backgroundGrey1;
}

  
</style>