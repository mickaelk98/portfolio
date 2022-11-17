<script setup>
import ProjectCard from './ProjectCard.vue';
</script>

<template>
  <div class="project-list">
    <ProjectCard />
    <ProjectCard />
    <ProjectCard />
    <ProjectCard />
    <ProjectCard />
    <ProjectCard />
  </div>
</template>

<style scoped lang="scss">
.project-list {
  margin: 0 auto;
  max-width: 1300px;
}

// Tablette
@media screen and (min-width: 768px) and (max-width: 1023px) {
  .project-list {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
}


@media screen and (min-width: 1024px) {
  .project-list {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
  }
}
</style>
