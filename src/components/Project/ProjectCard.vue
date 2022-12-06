<script setup>
import data from '../../data/project'
</script>

<template>
  <article v-for="project in data" :key="project.id">
    <div class="image-container">
      <img :src="project.image" :alt="project.imageDescription">
    </div>
    <h3>{{ project.title }}</h3>
    <ul>
      <li v-for="technologie in project.technologies">{{ technologie }}</li>
    </ul>
    <p>{{ project.description }}</p>
    <div class="buttons">

      <!-- lien vers le site du projet -->
      <a :href="project.siteLink" target="_blank">
        <button class="btn">Voir le projet</button>
      </a>

      <!-- lien vers le code du projet -->
      <a :href="project.codeLink" target="_blank">
        <button class="btn">Voir le code</button>
      </a>
    </div>
  </article>
</template>

<style scoped lang="scss">
article {
  width: 90%;
  max-width: 400px;
  margin: 20px auto 30px;

  .image-container {
    overflow: hidden;
    max-height: 185px;

    img {
      transition: transform 0.6s;
      width: 100%;
    }
  }

  h3 {
    text-transform: uppercase;
    margin: 5px 0;
  }

  p {
    color: var(--text-gray-color);
    margin: 20px 0;
  }

  ul {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    color: var(--tertiary-color);
    text-transform: uppercase;
  }

  .buttons {
    width: 90%;
    margin: 10px 0;
    display: flex;
    gap: 20px;

    .btn {
      text-transform: uppercase;
      letter-spacing: 2px;
      padding: 8px 5px;
      background: none;
      border: 1px solid var(--tertiary-color);
      color: var(--text-color);
      cursor: pointer;
      max-width: 200px;

      &:hover {
        background: var(--tertiary-color);
      }
    }
  }
}
</style>
