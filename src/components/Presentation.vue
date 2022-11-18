<script setup>
import { onMounted } from 'vue';

// attend que le composant apparaiet sur le DOM
onMounted(() => {
  const title = document.querySelector('.text h1');
  const text = document.querySelector('.text p');

  // animation du titre
  new Typewriter(title, {
    deleteSpeed: 20
  })
    .changeDelay(80)
    .typeString('Salut, je suis <span style="color: #00a8ff">Mickael Keita</span> développeur web.')
    .pauseFor(300)
    .start()

  // attend la fin de la première animation
  setTimeout(() => {
    // animation du text de presentation
    new Typewriter(text, {
      deleteSpeed: 50
    })
      .changeDelay(50)
      .typeString("Ayant toujours été attiré par la programation et les nouvelles technologies, j'ai donc suivi une formation sur <span style='font-weight: bold; color: #fff'>OpenClassroom</span> afin d'acquérir de solides compétences. Sur ce site, vous verrez différents projets que j'ai réalisés sur des technologies telles que ")
      .typeString("<span style='color: #dd4a24; font-weight: bold'>HTML</span>")
      .pause(1000)
      .deleteChars(4)
      .changeDelay(100)
      .typeString("<span style='color: #0169ba; font-weight: bold'>CSS</span>")
      .pauseFor(700)
      .deleteChars(3)
      .typeString("<span style='color: #c66495; font-weight bold'>SASS</span>")
      .pauseFor(700)
      .deleteChars(4)
      .typeString("<span style='color: #efd91c; font-weight: bold'>JAVASCRIPT</span> et <span style='color: #3fb27f; font-weight: bold'>VUEJS</span>")
      .start()
  }, 5000)
})


</script>

<template>
  <section>
    <div class="container">

      <!-- Text de presentation -->
      <div class="text">
        <h1></h1>
        <p></p>
      </div>

      <!-- Bouttons -->
      <div class="buttons">
        <a href="#contact">
          <button class="btn">Me contacter</button>
        </a>
        <button class="btn">Telecharger CV</button>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
@import '../assets/base.scss';

section {
  background: url(../../public/images/bg.jpg) center/cover;
  height: calc(100vh - 80px);
  display: flex;
  align-items: center;
  justify-content: center;

  .container {
    text-align: center;
    display: flex;
    flex-direction: column;
    margin: auto;
    max-width: 1300px;

    .text {
      h1 {
        font-size: 30px;
        margin: 30px 0;
        text-transform: none;
      }

      p {
        color: var(--text-gray-color);
        margin: 0 5px 50px;
        font-size: 20px;
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
      .text {
        margin-bottom: 50px;

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
    }
  }
}

@media screen and (min-width: 1024px) {
  section {
    .container {
      .text {
        margin-left: 10px;
      }

      .buttons {
        width: 50%;
        margin: 10px auto 50px;
        justify-content: space-between;
        flex-direction: row;
      }
    }
  }
}
</style>
