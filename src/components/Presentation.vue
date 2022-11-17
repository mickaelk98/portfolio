<script setup>

</script>

<template>
  <section>
    <div class="container">
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
    </div>
  </section>
</template>

<style scoped lang="scss">
@import '../assets/base.scss';

section {
  background: var(--primary-color);

  .container {
    text-align: center;
    display: flex;
    flex-direction: column-reverse;
    margin: auto;
    max-width: 1300px;

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
}

// Tablette
@media screen and (min-width: 768px) and (max-width: 1023px) {
  section {
    .container {
      flex-direction: row;

      .text {
        h1 {
          font-size: 25px;
        }

        p {
          font-size: 20px;
        }
      }

      .buttons {
        width: 50%;
        margin: 10px auto 50px;
        justify-content: space-between;
        flex-direction: row;
      }

      .profil-picture {
        max-width: 500px;

        img {
          height: 100%;
        }
      }
    }
  }
}

@media screen and (min-width: 1024px) {
  section {
    .container {
      flex-direction: row;
      text-align: left;
    }
  }
}
</style>
