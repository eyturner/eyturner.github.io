<template>
  <div id="app">
    <!-- modal for contact -->
    <section class="">
      <div class="modal fade bd-example-modal-lg" id="contactModal" tabindex="-1"
      role="dialog" aria-labelledby="myLargeModalLabel" aria-hidden="true">
          <div class="modal-dialog modal-lg">
                <div class="modal-content">
                    <Contact/> <!-- where we utilized the newly imported component -->
                </div>
          </div>
      </div>
    </section>
    <Navigation/>
    <Title/>
    <About/>
    <Skills/>
    <Projects/>
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
import Contact from './components/Contact.vue';

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
    Contact,
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
