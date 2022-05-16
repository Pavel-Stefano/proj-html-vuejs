<template>
  <div id="app">
    <app-header />
    <main>
      <section-fitness />
      <section-form />
    </main>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import SectionFitness from './components/SectionFitness.vue'
import SectionForm from './components/SectionForm.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    SectionFitness,
    SectionForm,
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
</style>
