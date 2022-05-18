<template>
    <section class="copyright">
        <div class="container">
            <div class="left">
                <i class="fa-regular fa-copyright"></i>
                <p>Copyright 2015 | Avada Theme by <span>ThemeFusion</span> | All Rights Reserved | Powered by <span>WordPress</span></p>
            </div>
            
            <div class="icon-container">
                <div class="content-icon">
                    <i class="fa-brands fa-facebook-f"></i>
                    <span>facebook</span>
                </div>
                <div class="content-icon">
                    <i class="fa-brands fa-twitter"></i>
                    <span>twitter</span>
                </div>
                <div class="content-icon">
                    <i class="fa-brands fa-instagram"></i>
                    <span>instagram</span>
                </div>
                 <div class="content-icon">
                    <i class="fa-brands fa-youtube"></i>
                    <span>youtube</span>
                </div>
                
            </div>
        </div>
    </section>
   

</template>

<script>
export default {
  name: 'FooterCopy',
  data(){
      return {
          
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
.copyright {
    height: 100px;
    background-color: $backgroundBlack;
    color: $textWhite;
    .container {
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;
        .left {
            display: flex;
            align-items: center;
            p {
                margin: 0;
                span {
                    cursor: pointer;
                    &:hover {
                        color: $textRose1;
                        transition: 0.5s;
                    }
                }
            }
        }
         .icon-container {
            display: flex;
            .content-icon{
                width: 40px;
                height: 40px;
                background: $BackgroundRose1;
                margin-right: 15px;
                display: flex;
                justify-content: center;
                align-items: center;
                border-radius: 6px;
                cursor: pointer;
                position: relative;
                &:hover {
                    background-color: $backgroundBlack;
                    transition: 0.7s;
                    &:hover span {
                        opacity: 1;
                        transition: 1s;
                    }
                }
                i {
                font-size: 18px;
                }
                span {
                    position: absolute;
                    top: -25px;
                    font-size: 12px;
                    opacity: 0;
                }
            }
        }
    }
}


  
</style>