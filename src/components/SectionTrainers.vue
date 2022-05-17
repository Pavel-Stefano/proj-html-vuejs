<template>
    <section class="trainers text-center">

        <h2>{{title.toUpperCase()}}</h2>
        <img src="../assets/images/divider-xx-red.png" alt="">
        <div class="container">
            <div class="row">

                <!-- card dinamica -->
                <div class="card-trainers col-4" v-for="(trainer,index) in cardsTrainers" :key="index">
                    <!-- <img :src="require(card[index].image)" alt=""> -->
                    <img src="../assets/images/trainer1-400x297.jpg" alt="">
                    <div class="content-card">
                        <p>{{cardsTrainers[index].nome}}</p>
                        <p>{{cardsTrainers[index].ruolo}}</p>
                        <span>{{cardsTrainers[index].descrizione}}</span>
                        <div class="icon-container">
                            <div class="content-icon">
                                <i class="fa-brands fa-facebook-f"></i>
                            </div>
                            <div class="content-icon">
                                <i class="fa-brands fa-twitter"></i>
                            </div>
                            <div class="content-icon">
                                <i class="fa-brands fa-instagram"></i>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
            <button>{{textButton.toUpperCase()}}</button>
        </div>
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
                  image: `../assets/images/trainer1-400x297.jpg`,
                  descrizione: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Necessitatibus, saepe? Totam blanditiis tempore'
              },
              { 
                  nome: 'Anne Warren',
                  ruolo: 'Personal Trainer',
                  image: `../assets/images/trainer3-400x297.jpg`,
                  descrizione: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Necessitatibus, saepe? Totam blanditiis tempore'

              },
              { 
                  nome: 'Peter Rice',
                  ruolo: 'Personal Trainer',
                  image: `../assets/images/trainer4 -400x297.jpg`,
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
            margin-top: 20px;
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
                i {
                font-size: 25px;
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