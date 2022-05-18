<template>
    <section class="news text-center">

        <h2>{{title.toUpperCase()}}</h2>
        <img class="divider" src="../assets/images/divider-xx-red.png" alt="">
        <div class="container clearfix">
                <!-- card dinamica -->
                <div class="card-news" v-for="(item, index) in articles" :key="index">
                    <div class="image">
                        <img :src="require('../assets/images/' + item.image)" alt="">
                        <div class="overflow">
                            <!-- icone -->
                            <i class="fa-solid fa-link"></i>
                            <i class="fa-solid fa-magnifying-glass"></i>             
                        </div>
                    </div>
                    
                    <div class="content-card">
                        <h4>{{item.titleArticles}}</h4>
                        <span>{{item.textArticle}}</span>
                    </div>
                </div>
            </div>
            <button>{{textButton.toUpperCase()}}</button>
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
                  image: 'blog1-400x208.jpg',
                  textArticle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]'
              },
              { 
                  titleArticles: 'Nutritional advice that will keep you training',
                  image: 'blog6-800x800.jpg',
                  textArticle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]'
              },
              { 
                  titleArticles: 'Simple principles for your next workout',
                  image: 'trainer4-400x297.jpg',
                  textArticle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]'
              },
              { 
                  titleArticles: "To be number one, train like you're number two",
                  image: 'blog4-400x289.jpg',
                  textArticle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]'
              },
              { 
                  titleArticles: 'Top 5 mistakes every gym member makes',
                  image: 'trainer3-400x297.jpg',
                  textArticle: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Donec pretium, tortor vitae porttitor suscipit, sapien purus aliquet risus, eu finibus arcu ante nec risus.[...]'
              },
              { 
                  titleArticles: 'The myths of shedding body fat explored',
                  image: 'trainer1-400x297.jpg',
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
    .image {
        position: relative;
        &:hover .overflow {
            background: $textRose1;
            opacity: 0.7;
            width: 100%;
            transition: 1s;
            justify-content: center;
                i {
                    // transition: 5s;  da rifinire
                    opacity: 1;
                    display: block;
                }
            &:hover img {
            opacity: 0.7;
            transition: 1.2s;
            width: 100%;
            }
        }
    }
    h4 {
        cursor: pointer;
            &:hover {
                color: $textRose1;
                transition: 0.5s;
            }
        }
    

}
button {
    margin-top: 50px;
    padding: 10px 20px;
    background: none;
    color: $textWhite;
    border: 1px solid $textWhite;
}

.clearfix {
    clear: both;
    content: '';
    display: table;
}

.overflow {
    position: absolute;
    top: 0;
    bottom: 0;
    width: 0;
    display: flex;
    align-items: center;
    justify-content: flex-start;
    gap: 10px;
    i {
        display: none;
        font-size: 30px;
        opacity: 0;
        cursor: pointer;
    }
}

.divider {
    margin: 35px 0;
}
</style>