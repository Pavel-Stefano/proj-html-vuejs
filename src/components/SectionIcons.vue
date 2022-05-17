<template>
    <section class="form-icons">
        <div class="container">
            <div class="row">
                <div class="box col-3 text-center" v-for="(item,index) in items" :key="index">
                    
                    <!-- <div class="icons"><i class="`fa-solid + ' '`" item.icon></i></div> -->
                    <div class="icons"><i class="fa-solid fa-bicycle"></i></div>
                    <h5>{{items.title}}</h5>
                    <img src="../assets/images/divider-x-red.png" alt="">
                    <p>{{item.text}}</p>
                </div>
            </div>
        </div>
        
    </section>
   

</template>

<script>
export default {
  name: 'SectionIcons',
  data(){
      return {
         items: [
             {
                 icon: 'fa-bicycle',
                 title: 'Strength & Conditioning',
                 image: '"../assets/images/divider-x-red.png"',
                 text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestias dolor iste doloribus sit'
             },
             {
                 icon: 'fa-bicycle',
                 title: 'Fitness & Cardio',
                 image: '"../assets/images/divider-x-red.png"',
                 text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestias dolor iste doloribus sit'
             },
             {
                 icon: 'fa-bicycle',
                 title: 'Flexibility & Rest',
                 image: '"../assets/images/divider-x-red.png"',
                 text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestias dolor iste doloribus sit'
             },
             {
                 icon: 'fa-bicycle',
                 title: 'Health & Diet',
                 image: '"../assets/images/divider-x-red.png"',
                 text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestias dolor iste doloribus sit'
             }
         ]
      }
  },
   props: {
     msg: String
   },
   methods: {
       
   },
   mounted(){
    //    console.log(this.items[0].title)
   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/vars.scss';
.form-icons {
    height: 630px;
    background-image: url('../assets/images/gym_bkgd_bw-compressor.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-position-y: 20%;
    .container{
        height: 100%;
        .row {
            height: 100%;
            display: flex;
            align-items: center;
            gap: 20px;
            flex-wrap: nowrap;
            color: $textWhite;
            .box {
                padding: 0px 30px;
            }
        }
    }
    .icons {
        margin: 20px 0;
    }
    .icons i {
        font-size: 40px;
        color: $BackgroundRose1;
        border: 1px solid $BackgroundRose1;
        border-radius: 50%;
        padding: 20px;
    }
    .box img {
        padding: 20px 0;
    }
    
}

  
</style>