<template>
    <section class="testimonial text-center">
        <div class="testimonial-content">
            <p>{{text}}</p>
            <img src="../assets/images/divider-white-xx.png" alt="">
            <h5>{{author.toUpperCase()}}</h5>
        </div>
        <!-- <p>"I fear not the man who has practiced 10,000 <br>
        kicks once, but I fear the man who has <br>
        practiced one kick 10,000 times"</p> -->
        
        <!-- <h5>Bruce lee . quote of the day</h5> -->
        

    </section>
   

</template>

<script>
export default {
  name: 'SectionTestimonial',
  data(){
      return {
          text:`"I fear not the man who has practiced 10,000
        kicks once, but I fear the man who has
        practiced one kick 10,000 times"`,
        author: 'Bruce lee . quote of the day'
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

.testimonial {
    height: 600px;
    background-image: url('../assets/images/home-testimonial-bg.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-position-y: 45%;
    color: $textWhite;
    display: flex;
    justify-content: center;
    align-items: center;
    img {
        position: relative;
        bottom: 25px;
    }
    p {
        font-size: 31px;
        position: relative;
        bottom: 23px;
    }
    .testimonial-content {
        width: 660px;
    }
    h5{
        font-weight: revert;
    }
}

  
</style>