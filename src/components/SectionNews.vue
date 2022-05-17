<template>
    <section class="news text-center">

        <h2>{{title.toUpperCase()}}</h2>
        <img src="../assets/images/divider-xx-red.png" alt="">
        <div class="container">
            <div class="row">

                <div class="card-news col-4">
                    <!-- <img :src="require(card[index].image)" alt=""> -->
                    <img src="../assets/images/blog1-400x208.jpg" alt="">
                    <div class="content-card">
                        <h4>Train with free weights or your body weight?</h4>
                        <span>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]</span>
                    </div>
                </div>

                <div class="card-news col-4">
                    <!-- <img :src="require(card[index].image)" alt=""> -->
                    <img src="../assets/images/blog6-800x800.jpg" alt="">
                    <div class="content-card">
                        <h4>Train with free weights or your body weight?</h4>
                        <span>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]</span>
                    </div>
                </div>

                <div class="card-news col-4">
                    <!-- <img :src="require(card[index].image)" alt=""> -->
                    <img src="../assets/images/trainer4-400x297.jpg" alt="">
                    <div class="content-card">
                        <h4>Train with free weights or your body weight?</h4>
                        <span>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]</span>
                    </div>
                </div>

                <div class="card-news col-4">
                    <!-- <img :src="require(card[index].image)" alt=""> -->
                    <img src="../assets/images/blog4-400x289.jpg" alt="">
                    <div class="content-card">
                        <h4>Train with free weights or your body weight?</h4>
                        <span>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]</span>
                    </div>
                </div>

                <div class="card-news col-4">
                    <!-- <img :src="require(card[index].image)" alt=""> -->
                    <img src="../assets/images/trainer3-400x297.jpg" alt="">
                    <div class="content-card">
                        <h4>Train with free weights or your body weight?</h4>
                        <span>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]</span>
                    </div>
                </div>

                <div class="card-news col-4">
                    <!-- <img :src="require(card[index].image)" alt=""> -->
                    <img src="../assets/images/trainer1-400x297.jpg" alt="">
                    <div class="content-card">
                        <h4>Train with free weights or your body weight?</h4>
                        <span>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]</span>
                    </div>
                </div>

                <!-- card dinamica -->
                <!-- <div class="card-news col-4" v-for="(article,index) in articles" :key="index"> -->
                    <!-- <img :src="require(card[index].image)" alt=""> -->
                    <!-- <img src="../assets/images/trainer1-400x297.jpg" alt="">
                    <div class="content-card">
                        <h4>{{article[index].titleArticles}}</h4>
                        <span>{{article[index].textArticle}}</span> -->
                    <!-- </div>
                </div> -->

            </div>
            <button>{{textButton.toUpperCase()}}</button>
        </div>
    </section>
   

</template>

<script>
export default {
  name: 'SectionNews',
  data(){
      return {
          title: 'Performance News',
          articles: [
              { 
                  titleArticles: 'Train with free weights or your body weight?',
                  image: `../assets/images/blog1-400x208.jpg`,
                  textArticle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]'
              },
              { 
                  titleArticles: 'Nutritional advice that will keep you training',
                  image: `../assets/images/blog6-800x800.jpg`,
                  textArticle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]'
              },
              { 
                  titleArticles: 'Simple principles for your next workout',
                  image: `../assets/images/trainer4-400x297.jpg`,
                  textArticle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]'
              },
              { 
                  titleArticles: "To be number one, train like you're number two",
                  image: `../assets/images/blog4-400x289.jpg`,
                  textArticle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]'
              },
              { 
                  titleArticles: 'Top 5 mistakes every gym member makes',
                  image: `../assets/images/trainer3-400x297`,
                  textArticle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]'
              },
              { 
                  titleArticles: 'The myths of shedding body fat explored',
                  image: `../assets/images/trainer1-400x297.jpg`,
                  textArticle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]'
              },
              
          ],
          textButton: 'Read all articles'
      }
  },
//   props: {
//     msg: String
//   }
mounted(){
    
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/vars.scss';

.news{
    background-color: $backgroundGrey1;
    color: $textWhite;
    padding: 100px 0;
    .card-news {
        margin: 20px;
        width: calc(100% / 3 - 40px);
        float: left;
        .content-card {
            text-align: left;
            padding: 30px;
            background: $backgroundGrey2;
        }
        
        img {
            width: 100%;
        }
        h2 {
            font-size: 40px;
            font-weight: 900;
        }
        span {
            font-size: 17px;
            box-sizing: border-box;
            text-align: left;
        }
    }
    img {
        padding: 35px 0 0;
        }

}
button {
    margin-top: 50px;
    padding: 10px 20px;
    background: none;
    color: $textWhite;
    border: 1px solid $textWhite;
}
  
</style>