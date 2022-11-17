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
    <TheFooter class="db6" />
  </div>
</template>

<style lang="scss">
@import './assets/base.scss';
// @import './assets/debug.scss';


// Mobile
@media screen and (min-width: 767px) {}

// Tablette
@media screen and (min-width: 768px) and (max-width: 1023px) {}

// Ordinateur
@media screen and (min-width: 1024px) {}
</style>
