<template>
    <section class="form-section">
        <div class="container">
            <div class="row">
                 <div class="col-6 box-img">
                    <img src="../assets/images/home_img-compressor.jpg" alt="">
                </div>

                <div class="col-6 box-form">
                    <h4>{{subTitle}}</h4>
                    <span>Name..*</span>
                    <input type="text">
                    <span>Email</span>
                    <input type="text">
                    <button>{{textButton.toUpperCase()}}</button>
                </div>
            </div>
        </div>

    </section>
   

</template>

<script>
export default {
  name: 'SectionForm',
  data(){
      return {
          subTitle: 'Sing up for a free training session!',
          textButton:'Start now!'
      }
  },
   props: {
     msg: String
   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/vars.scss';
.form-section {
    padding: 150px 0;
    background-color: $backgroundGrey2;
    color: $textWhite;
    display: flex;
    align-items: center;
}

.box-form {
    display: flex;
    flex-direction: column;
    gap: 7px;
}

h4 {
    margin-bottom: 50px;
}
input {
    margin-bottom: 25px;
    background-color: $backgroundGrey2;
    border: 1px solid $backgroundBlue1;
}
input {
    padding: 5px;
}
button {
    margin-top: 15px;
    padding: 15px;
    background-color: $BackgroundRose1;
    color: $textWhite;
}
  
</style>