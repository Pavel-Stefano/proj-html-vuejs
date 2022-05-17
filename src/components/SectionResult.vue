<template>
    <section class="result text-center">

        <h2>{{title.toUpperCase()}}</h2>
        <img src="../assets/images/divider-xx-red.png" alt="">
        <div class="container">
            <div class="row">
                <div class="card-result" v-for="(card, index) in people" :key="index">
                    <div class="box-image"> 
                        <img :src="require('../assets/images/' + card.image)" alt="">
                    </div>
                    <div class="box-text">
                        <span>{{card.descriptions}}</span>
                        <h6>-{{card.nome}}</h6>

                    </div>
                </div>
            </div>
        </div>
    </section>
   

</template>

<script>
export default {
  name: 'SectionResult',
  data(){
      return {
          title: 'Real world result',
          people: [
              {
                  nome: 'Tara Smith',
                  image: 'review_1-compressor.jpg',
                  descriptions: '"The trainers at Avada Gym have helped me reach my fitness goals beyond anything I could of hoped for.I love it!"'

              },
              {
                  nome: 'Simon Chel',
                  image: 'review_3-compressor-2.jpg',
                  descriptions: '"The atmosphere at Avada Gym is amazing, the people are even better. All in all, it is a great place to work out."'

              },
              {
                  nome: 'Jen Wirth',
                  image: 'review_2-compressor.jpg',
                  descriptions: '"The facilities at Avada Gym stood out to me the most. They are well maintained and have high quality equipment."'
              },
              {
                  nome: 'Jeff Glum',
                  image: 'review_4-compressor-2.jpg',
                  descriptions: '"No bad things to say about Avada Gym, they are top notch at every corner and truly take care of their customers."'
              }
          ]
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

.result{
    background-color: $backgroundGrey1;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    color: $textWhite;
    padding: 100px 0;
    .card-result {
        background-color: #212425;
        display: flex;
        align-items: center;
        padding: 20px 40px;
        height: 200px;
        margin: 20px;
        width: calc(100% / 2 - 40px);
        gap: 35px;
        h2 {
            font-size: 40px;
            font-weight: 900;
        }
        span {
            font-style: oblique;
            font-size: 17px;
            box-sizing: border-box;
            text-align: left;
        }
    }
    img {
        padding: 35px 0;
        }
    .box-text {
        text-align: left;
    }
    h6 {
        margin-top: 15px;
    }
}

  
</style>