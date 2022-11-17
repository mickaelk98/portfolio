<script setup>
import TheHeader from './components/TheHeader.vue';
import TheFooter from './components/TheFooter.vue'
import Contact from './components/Contact.vue'
import Presentation from './components/Presentation.vue';
import TechnoList from './components/TechnoList.vue';
import Project from './components/Project/Project.vue';
</script>

<template>
  <div class="page-container">
    <TheHeader />
    <Presentation />
    <TechnoList />
    <Project />
    <Contact />
    <TheFooter />
  </div>
</template>

<style lang="scss">
@import './assets/base.scss';
// @import './assets/debug.scss';

// .page-container {
//   display: block;
//   margin: auto;
//   max-width: 1200px;
//   padding: 0 1rem;
// }
</style>
