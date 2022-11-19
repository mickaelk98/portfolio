<script setup>

</script>

<template>
  <section id="contact">
    <div class="container">
      <div class="contact-text">
        <h2>contact</h2>
        <p>N'hésitez pas à me contacter, je vous répondrai le plus tôt possible.</p>
      </div>
      <form name="contact" method="post" netlify>
        <input type="text" name="nom" placeholder="Nom">
        <input type="text" name="email" placeholder="Email">
        <textarea name="message" placeholder="Votre message"></textarea>
        <button class="btn">Envoyer</button>
      </form>
    </div>
  </section>
</template>

<style scoped lang="scss">
@import '../assets/base.scss';

section {
  background: var(--secondary-color);
  text-align: center;

  .container {
    max-width: 1300px;
    margin: auto;

    .contact-text {
      margin-bottom: 30px;

      h2 {
        padding: 30px;
      }

      p {
        color: var(--text-gray-color);
        font-size: 20px;
        margin: 0 10px;
      }
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 20px;
      width: 80%;
      margin: 0 auto;

      input,
      textarea {
        padding: 10px;
        background: none;
        border: none;
        outline: none;
        border-bottom: 1px solid var(--text-gray-color);
        color: var(--text-gray-color);
      }

      textarea {
        resize: none;
        height: 120px;
      }

      .btn {
        text-transform: uppercase;
        letter-spacing: 2px;
        padding: 8px;
        background: none;
        border: 1px solid var(--tertiary-color);
        color: var(--text-color);
        cursor: pointer;
        max-width: 200px;
        align-self: flex-end;
        margin: 20px 0 50px;

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
      form {
        display: flex;
        flex-direction: column;
        gap: 20px;
        width: 60%;
        margin: 0 auto;
      }
    }
  }
}

@media screen and (min-width: 1024px) {
  section {
    .container {
      display: flex;
      gap: 30px;

      padding: 30px 0;

      form {
        display: flex;
        flex-direction: column;
        gap: 20px;
        max-width: 700px;
        margin: 0 10px;
      }
    }
  }
}
</style>
