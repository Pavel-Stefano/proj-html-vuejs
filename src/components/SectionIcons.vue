<template>
    <section class="form-icons">
        <div class="container">
            <div class="row">
                <div class="box col-3 text-center" v-for="(item,index) in items" :key="index">
                    <div class="top">
                        <div class="icons"><i class="fa-solid fa-bicycle"></i></div>
                        <h5>{{item.title}}</h5>
                    </div>
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
        position: relative;
        &:hover {
            transform: scale(0.9);
            transition: 0.5s;
        }
        &:hover:after {
            transform: scale(1.5);
            transition: 0.5s;
            // animation: circle-up 5s cubic-bezier 3s linear;
        }
        // @keyframes circle-up {
        //     0% {
        //         transform: scale(1);
        //     }
        //     50% {
        //         transform: scale(1.5);
        //     }
        //     80%, 100% {
        //         opacity: 0;
        //     }
        // }
        &::after {
            content: "";
            position: absolute;
            display: block;
            /* width: 300%; */
            top: 0;
            left: 0;
            bottom: 0;
            right: 0;
            border: 1px solid $textRose1;
            border-radius: 50%;
            box-shadow: 0 0 8px rgba(0,0,0,.3);
            // animation: pulse-dot 1.25s cubic-bezier(0.455, 0.03, 0.515, 0.955) -.4s infinite;
        }
        // @keyframes pulse-ring {
        //     0% {
        //         transform: scale(.33);
        //     }
        //     80%, 100% {
        //         opacity: 0;
        //     }
        // }

        // @keyframes pulse-dot {
        //     0% {
        //         transform: scale(.8);
        //     }
        //     50% {
        //         transform: scale(1);
        //     }
        //     100% {
        //         transform: scale(.8);
        //     }
        // }
    }


    .box img {
        padding: 20px 0;
    }
    .top {
        cursor: pointer;
            &:hover h5 {
                color: $textRose1;
                transition: 0.5s;
            }
        }
}

  
</style>