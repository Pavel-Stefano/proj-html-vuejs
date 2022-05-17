<template>
  <div id="app">
    <app-header />
    <main>
      <section-fitness />
      <section-form />
      <section-icons />
      <section-result />
    </main>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import SectionFitness from './components/SectionFitness.vue'
import SectionForm from './components/SectionForm.vue'
import SectionIcons from './components/SectionIcons.vue'
import SectionResult from './components/SectionResult.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    SectionFitness,
    SectionForm,
    SectionIcons,
    SectionResult,
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
