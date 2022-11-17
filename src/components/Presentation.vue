<script setup>

</script>

<template>
  <section>
    <!-- Text de presentation -->
    <div class="text">
      <h1>Salut moi c'est <span>Mickael Keita</span>, je suis developpeur web</h1>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt at ex quaerat
        reprehenderit assumenda, suscipit blanditiis quas architecto
        modi!
      </p>
      <div class="buttons">
        <button class="btn">Me contacter</button>
        <button class="btn">Telecharger CV</button>
      </div>
    </div>

    <!-- image -->
    <div class="profil-picture">
      <img src="../../public/images/unsplash-profil-sans-bg.png" alt="profil">
    </div>
  </section>
</template>

<style scoped lang="scss">
@import '../assets/base.scss';

section {
  background: var(--primary-color);
  text-align: center;
  display: flex;
  flex-direction: column-reverse;

  .profil-picture {
    background: var(--secondary-color);
    margin: 0 auto;
    max-width: 250px;
    border-radius: 0 0 10px 10px;
  }

  .text {
    h1 {
      margin: 30px 0;

      span {
        text-decoration: underline var(--tertiary-color);
      }
    }

    p {
      color: var(--text-gray-color);
      margin: 0 5px 50px;
    }
  }

  .buttons {
    width: 90%;
    margin: 10px auto 50px;
    display: flex;
    flex-direction: column;
    gap: 20px;
    justify-content: space-between;

    .btn {
      text-transform: uppercase;
      letter-spacing: 2px;
      padding: 8px;
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
