<template>
  <div id="app">
    <Navigation/>
    <Title/>
    <About></About>
    <Projects/>
    <Skills/>
    <Work/>
    <ResumePDF/>
  </div>
</template>

<script>

import Title from './components/Title.vue';
import About from './components/About.vue';
import Navigation from './components/Navigation.vue';
import Skills from './components/Skills.vue';
import Projects from './components/Projects.vue';
import Work from './components/Work.vue';
import ResumePDF from './components/ResumePDF.vue';

export default {
  name: 'App',
  components: {
    Navigation,
    Title,
    About,
    Skills,
    Projects,
    Work,
    ResumePDF,
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

html {
  scroll-behavior: smooth;
}
</style>
