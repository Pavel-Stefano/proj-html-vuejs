<template>
  <div id="app">
    <app-header />
    <main>
      <section-fitness />
      <section-form />
      <section-icons />
      <section-result />
      <section-performance />
      <section-testimonial />
    </main>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import SectionFitness from './components/SectionFitness.vue'
import SectionForm from './components/SectionForm.vue'
import SectionIcons from './components/SectionIcons.vue'
import SectionPerformance from './components/SectionPerformance.vue'
import SectionResult from './components/SectionResult.vue'
import SectionTestimonial from './components/SectionTestimonial.vue'


export default {
  name: 'App',
  components: {
    AppHeader,  
    SectionFitness,
    SectionForm,
    SectionIcons,     //icons da rifinire stampare icone / importare icone che ora le prendo con la cdn
    SectionResult,    //result da rifinire stampare immagini 
    SectionPerformance,
    SectionTestimonial,       
  }
}
</script>

<style lang="scss">
@import './style/generals.scss';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.debug {
  border: 1px solid black;
}
</style>
