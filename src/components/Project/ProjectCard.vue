<script setup>

</script>

<template>
  <article>
    <img src="../../../public/images/unsplash-cart.jpg" alt="phot du projet">
    <h3>Titre du projet</h3>
    <ul>
      <li>HTML</li>
      <li>CSS</li>
    </ul>
    <div class="buttons">
      <button class="btn">Voir le projet</button>
      <button class="btn">Voir le code</button>
    </div>
  </article>
</template>

<style scoped lang="scss">
article {
  width: 90%;
  margin: 20px auto 30px;

  h3 {
    text-transform: uppercase;
    margin: 5px 0;
  }

  ul {
    display: flex;
    gap: 10px;
    color: var(--text-gray-color);
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
