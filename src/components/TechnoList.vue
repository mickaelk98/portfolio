<script setup>

</script>

<template>
  <section>
    <ul>
      <!-- html -->
      <li>
        <i class="devicon-html5-plain-wordmark colored"></i>
      </li>
      <!-- css -->
      <li>
        <i class="devicon-css3-plain-wordmark colored"></i>
      </li>
      <!-- sass -->
      <li>
        <i class="devicon-sass-original colored"></i>
      </li>
      <!-- javascript -->
      <li>
        <i class="devicon-javascript-plain colored"></i>
      </li>
      <!-- vuejs -->
      <li>
        <i class="devicon-vuejs-plain-wordmark colored"></i>
      </li>
      <!-- nodejs -->
      <li>
        <i class="devicon-nodejs-plain colored"></i>
      </li>
      <!-- mongoDb -->
      <li>
        <i class="devicon-mongodb-plain-wordmark colored"></i>
      </li>
    </ul>
  </section>
</template>

<style scoped lang="scss">
@import '../assets/base.scss';

section {
  position: relative;
  padding: 30px 0;
  background: var(--secondary-color);

  ul {
    text-align: center;
    margin: auto;
    max-width: 1300px;

    li {
      font-size: 70px;
    }
  }
}

// Tablette
@media screen and (min-width: 768px) and (max-width: 1023px) {
  section {
    ul {
      display: flex;
      justify-content: space-around;
    }
  }
}

@media screen and (min-width: 1024px) {
  section {
    ul {
      display: flex;
      justify-content: space-between;
    }
  }
}
</style>
