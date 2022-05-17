<template>
    <section class="performance text-center">

        <h2>{{title.toUpperCase()}}</h2>
        <img src="../assets/images/divider-xx-red.png" alt="">
        <div class="container">
            <div class="row">
                <div class="card-performance col-4" v-for="(card,index)  in images" :key="index">
                    <!-- <img :src="require(card[index].image)" alt=""> -->
                    <img :src="require('../assets/images/' + card.image)" alt="">
                </div>
            </div>
        </div>
    </section>
   

</template>

<script>
export default {
  name: 'SectionPerformance',
  data(){
      return {
          title: 'High performance facilities',
          images: [
              { 
                  image: `home-image1.jpg`
              },
              { 
                  image: `home-image2.jpg`
              },
              { 
                  image: `home-image3.jpg`
              },
              { 
                  image: `home-image4.jpg`
              },
              { 
                  image: `home-image54.jpg`
              },
              { 
                  image: `home-image6.jpg`
              },
              
             
          ]
      }
  },
//   props: {
//     msg: String
//   }
mounted(){
    console.log(this.images)
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/vars.scss';

.performance{
    background-color: $backgroundGrey1;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    color: $textWhite;
    padding: 100px 0;
    .card-performance {
        display: flex;
        margin: 20px;
        width: calc(100% / 3 - 40px);
        
        img {
            width: 100%;
        }
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

}

  
</style>