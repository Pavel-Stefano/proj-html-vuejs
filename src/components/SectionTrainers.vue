<template>
    <section class="trainers text-center">

        <h2>{{title.toUpperCase()}}</h2>
        <img src="../assets/images/divider-xx-red.png" alt="">
        <div class="container">
            <div class="row">

                <!-- card dinamica -->
                <div class="card-trainers col-4" v-for="(trainer,index) in cardsTrainers" :key="index">
                    <img :src="require('../assets/images/' + trainer.image)" alt="">
                    <div class="content-card">
                        <p>{{trainer.nome}}</p>
                        <p>{{trainer.ruolo}}</p>
                        <span>{{trainer.descrizione}}</span>
                        <div class="icon-container text-center">
                            <div class="content-icon">
                                <i class="fa-brands fa-facebook-f"></i>
                                <span>
                                    facebook
                                    <i class="fa-solid fa-square-full"></i>
                                </span>
                            </div>
                            <div class="content-icon">
                                <i class="fa-brands fa-twitter"></i>
                                <span>
                                    twitter
                                    <i class="fa-solid fa-square-full"></i>
                                </span>
                            </div>
                            <div class="content-icon">
                                <i class="fa-brands fa-instagram"></i>
                                <span>
                                    instagram
                                    <i class="fa-solid fa-square-full"></i>
                                </span>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
            <button>{{textButton.toUpperCase()}}</button>
        </div>
        <i class="icon fa-solid fa-square-full"></i>
    </section>
   

</template>

<script>
export default {
  name: 'SectionTrainers',
  data(){
      return {
          title: 'Meet our trainers',
          cardsTrainers: [
              { 
                  nome: 'Ann Baker',
                  ruolo: 'Personal Trainer',
                  image: 'trainer1-400x297.jpg',
                  descrizione: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Necessitatibus, saepe? Totam blanditiis tempore'
              },
              { 
                  nome: 'Anne Warren',
                  ruolo: 'Personal Trainer',
                  image: 'trainer3-400x297.jpg',
                  descrizione: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Necessitatibus, saepe? Totam blanditiis tempore'

              },
              { 
                  nome: 'Peter Rice',
                  ruolo: 'Personal Trainer',
                  image: 'trainer4-400x297.jpg',
                  descrizione: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Necessitatibus, saepe? Totam blanditiis tempore'

              },
          ],
          textButton: 'View all trainers'
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

.trainers{
    background-color: $backgroundGrey2;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    color: $textWhite;
    padding: 100px 0;
    position: relative;
    .card-trainers {
        display: flex;
        flex-direction: column;
        margin: 20px;
        width: calc(100% / 3 - 40px);
        .content-card {
            text-align: left;
            padding: 30px;
            background: $backgroundGrey1;
        }

        .icon-container {
            margin-top: 35px;
            display: flex;
            .content-icon{
                width: 40px;
                height: 40px;
                background: $backgroundGrey2;
                margin-right: 15px;
                display: flex;
                justify-content: center;
                align-items: center;
                border-radius: 6px;
                cursor: pointer;
                position: relative;
                    &:hover span {
                        opacity: 1;
                        transition: 0.7s;
                    }
                .fa-brands {
                font-size: 25px;
                }
                span {
                    position: absolute;
                    top: -30px;
                    font-size: 12px;
                    opacity: 0;
                    background: $backgroundGrey2;
                    padding: 2px 6px;
                    border-radius: 5px;
                    i {
                       position: absolute;
                        bottom: -4px;
                        left: 40%;
                        transform: rotate(45deg);
                        font-size: 8px;
                        color: $backgroundGrey2;
                    }
                }
            }
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
            &:hover {
                transform: scale(1.1);
                transition: 0.8s;

                // animation: scaleImg 2s linear;
                // @keyframes scaleImg {
                //     0% {
                //         transform: scale(0);
                //     }
                //     50% {
                //         transform: scale(1.1);
                //     }
                //     100% {
                //         transform: scale(01.1);
                //     }
                // }
                box-shadow: 10px 10px 8px $backgroundGrey2;
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

i.icon {
    color: $backgroundGrey2;
    position: absolute;
    bottom: -26px;
    transform: rotate(45deg);
    font-size: 50px;
    border: 1px solid $backgroundGrey2;
}

  
</style>