<script setup>
import ProjectList from './ProjectList.vue';
</script>

<template>
  <section>
    <h2>Projets</h2>
    <ProjectList />
  </section>
</template>

<style scoped lang="scss">
@import '../../assets/base.scss';

section {
  background: var(--primary-color);
  padding: 30px 0;

  h2 {
    margin: 0 10px 20px;
  }
}
</style>
