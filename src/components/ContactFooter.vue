<template>
    <section class="contact-footer">
        <div class="container">
            <div class="row">
                <div class="box contact col-3">
                    <div class="title">{{titoloContact.toUpperCase()}}</div>
                    <ul>
                        <li v-for="link in info" :key="link">{{link.contact}}</li>
                    </ul>
                </div>
                <div class="box post col-3">
                    <div class="title">{{titoloPost.toUpperCase()}}</div>
                    <p v-for="text in postRecenti" :key="text"> > {{text.post}}</p>
                </div>
                <div class="box col-3">
                    <div class="title">{{titoloApertura.toUpperCase()}}</div>
                    <div class="content" v-for="open in openingTimes" :key="open">
                        <p>{{open.opening}}</p>
                        <span>{{open.times}}</span>
                    </div >
                    

                </div>
                <div class="col-3">
                    <img src="../assets/images/gym_ad-compressor.jpg" alt="">
                </div>
            </div>
        </div>
        
    </section>
   

</template>

<script>
export default {
  name: 'ContactFooter',
  data(){
      return {
        titoloContact: 'Come find us',
        info: [
            {
                contact:'12345 North Main Street',
            },
            {
                contact:'New York, NY 555555',
            },
            {
                contact:'Phone:1.800.555.6789',
            },
            {
                contact:'Email:info@your-domain.com',
            },
        ],
        titoloPost: 'Recent posts',
        postRecenti:[
            {
                post:'Train with free weights or your body weight?',
            },
            {
                post:'Nutritional advice that will keep you training',
            },
        ],
        titoloApertura: 'Opening times',
        openingTimes:[
            {
                opening:'Weekdays Monday - Friday',
                times: '09.00 - 19.00'
            },
            {
                opening:'Weekends: Saturday - Sunday',
                times: '09.00 - 21.00'
            },
        ]
      }
  },
   props: {
     msg: String
   },
   methods: {
       
   },
   mounted(){
    console.log(this.info)
   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/vars.scss';
.contact-footer {
    height: 500px;
    background-color: $backgroundGrey2;
    .container{
        height: 100%;
        padding-top: 150px;
        .row {
            height: 100%;
            display: flex;
            gap: 20px;
            flex-wrap: nowrap;
            color: $textWhite;
        }
    }
    
}
.title, span {
    color: $backgroundGrey3;
}
.contact {
    line-height: 30px;
    ul {
        padding-left: 0;
        li {
            list-style-type: none;
    }
    }
}

.post p {
    border-bottom: 1px solid grey;
    padding-bottom: 25px;
}
.post p:nth-child(3){
    margin-top: -18px;
}

.box {
    display: flex;
    flex-direction: column;
    gap: 20px;
}
</style>