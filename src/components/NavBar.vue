<template>
    <div class="nav-bar">
        <ul>
            <li v-for="link in links" :key="link">{{link}}</li>
        </ul>
    </div>

</template>

<script>
export default {
  name: 'NavBar',
  data(){
      return {
          links: [
              'Home',
              'About Us',
              'Facilities',
              'Membership',
              'Testimonials',
              'Blog'
          ]
      }
  },
//   props: {
//     msg: String
//   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@import '../style/vars.scss';
.nav-bar {
    display: flex;
    align-items: center;
    ul {
        display: flex;
        li {
        margin: 0 12px;
        text-transform: uppercase;
        list-style-type: none;
        cursor: pointer;
            &:hover  {
                color: $textRose1,      
            }
        }
    }
}

  
</style>