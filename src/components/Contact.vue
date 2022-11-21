<script setup>
import { useField, useForm } from 'vee-validate';
import { z } from 'zod'
import { toFormValidator } from '@vee-validate/zod'
import emailjs from '@emailjs/browser';
import EMAILJS_PUBLICKEY from '../data/emailjsKey';

// verification des saisies de l'utilisateur
const validationSchema = toFormValidator(
  z.object({
    name: z.string({ required_error: "Ce champ est obligatoire" })
      .regex(new RegExp("^([a-z]+(( |')[a-z]+)*)+([-]([a-z]+(( |')[a-z]+)*)+)*$"), "Votre nom nest pas conforme")
      .max(50, "votre nom doit faire moin de 50 caractères"),
    email: z.string({ required_error: "Ce champ est obligatoire" })
      .email("Vous devez rentrez une adresse email"),
    subject: z.string({ required_error: "Ce champ est obligatoire" })
      .min(1, "Ce champ ne peut pas etre vide")
      .max(100, "Votre sujet ne doit pas depasser 100 caractères"),
    message: z.string({ required_error: "Ce champ est obligatoire" })
      .min(1, "Ce champ ne peut pas etre vide")
      .max(1000, "Votre message doit faire maximum de 1000 caractères"),
  })
)

// acceder au données a la soumission du formulaire
const { handleSubmit, setErrors } = useForm({ validationSchema })


// capture des saisies de l'utilisateur
const { value: nameValue, errorMessage: nameError } = useField("name");
const { value: emailValue, errorMessage: emailError } = useField("email")
const { value: subjectValue, errorMessage: subjectError } = useField("subject")
const { value: messageValue, errorMessage: messageError } = useField("message")


// fonction pour soummettre un formulaire
const sendMessage = handleSubmit(async (formValue, { resetForm }) => {
  try {
    const templateParams = {
      name: formValue.name,
      email: formValue.email,
      subject: formValue.subject,
      message: formValue.message
    };

    const templateID = "template_s55k1eg"
    const serviceID = "service_nkh4tr2"
    const publicKey = `${EMAILJS_PUBLICKEY}`

    const result = await emailjs.send(serviceID, templateID, templateParams, publicKey);

    if (result.status === 200) {
      resetForm()
      alert('Votre message a bien été envoyé')
    }

  } catch (e) {
    console.log(e);
  }
})

</script>

<template>
  <section id="contact">
    <div class="container">
      <div class="contact-text">
        <h2>contact</h2>
        <p>N'hésitez pas à me contacter, je vous répondrai le plus tôt possible.</p>
      </div>
      <form @submit="sendMessage">
        <!-- nom -->
        <input v-model="nameValue" type="text" placeholder="Nom">
        <small v-if="nameError">{{ nameError }}</small>

        <!-- email -->
        <input v-model="emailValue" type="text" placeholder="Email">
        <small v-if="emailError">{{ emailError }}</small>

        <!-- sujet -->
        <input v-model="subjectValue" type="text" placeholder="Le sujet de votre message">
        <small v-if="subjectError">{{ subjectError }}</small>

        <!-- message -->
        <textarea v-model="messageValue" placeholder="Votre message"></textarea>
        <small v-if="messageError">{{ messageError }}</small>

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
