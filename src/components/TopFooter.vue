<template>
    <section class="top-footer">
        <div class="container">
            <div class="left">
                <h2>{{title}}</h2>
                <p>Flexible membership packages to suit all levels of athlete and achive your fitness goals</p>
            </div>

            <div class="right">
                <button>{{textButton.toUpperCase()}}</button>
            </div>
        </div>
    </section>
   

</template>

<script>
export default {
  name: 'TopFooter',
  data(){
      return {
          title: 'Achieve Your Fitness Goals',
          textButton: 'Join us'
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

.top-footer {
    background-image: url('../assets/images/home-parallax.jpg');
    background-position-y: 17%;
    height: 200px;
    color: $textWhite;
    .container {
        height: 100%;
        display: flex;
        align-items: center;
        .left {
            margin: 15px 0 0 40px;
            h2 {
            font-size: 30px;
            font-weight: 900;
            }
        }
    }
    p {
        font-size: 18px;
    }
    button {
    margin-left: 250px;
    padding: 15px 30px;
    background: none;
    color: $textWhite;
    border: 1px solid $textWhite;
    }
}

  
</style>