<script setup>
import ProjectList from './ProjectList.vue';
</script>

<template>
  <section>
    <div class="container">
      <h2>Projets</h2>
      <ProjectList />
    </div>
  </section>
</template>

<style scoped lang="scss">
@import '../../assets/base.scss';

section {
  background: var(--primary-color);
  padding: 30px 0;

  .container {
    max-width: 1300px;
    margin: auto;

    h2 {
      margin: 0 10px 20px;
    }
  }
}
</style>
