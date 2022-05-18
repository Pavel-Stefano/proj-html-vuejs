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
      <section-trainers />
      <section-news />
    </main>
    <footer>
      <top-footer />
      <contact-footer />
      <footer-copy />
    </footer>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import ContactFooter from './components/ContactFooter.vue'
import FooterCopy from './components/FooterCopy.vue'
import SectionFitness from './components/SectionFitness.vue'
import SectionForm from './components/SectionForm.vue'
import SectionIcons from './components/SectionIcons.vue'
import SectionNews from './components/SectionNews.vue'
import SectionPerformance from './components/SectionPerformance.vue'
import SectionResult from './components/SectionResult.vue'
import SectionTestimonial from './components/SectionTestimonial.vue'
import SectionTrainers from './components/SectionTrainers.vue'
import TopFooter from './components/TopFooter.vue'


export default {
  name: 'App',
  components: {
    AppHeader,  
    SectionFitness,
    SectionForm,
    SectionIcons,     //icons da rifinire stampare icone / importare icone che ora le prendo con la cdn
    SectionResult, 
    SectionPerformance,
    SectionTestimonial,
    SectionTrainers,  
    SectionNews,
    TopFooter,
    ContactFooter,
    FooterCopy,
           
  }
}
</script>

<style lang="scss">
@import './style/generals.scss';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  max-width: 1884px;
}

h2 {
  font-weight: 900;
}

button {
  opacity: 0.8;
  &:hover {
    opacity: 1;
  }
}

.debug {
  border: 1px solid black;
}
</style>
