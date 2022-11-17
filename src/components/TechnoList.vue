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
  background: var(--primary-color);

  &::before {
    content: "";
    position: absolute;
    top: 0;
    left: 10px;
    right: 10px;
    height: 2px;
    // width: 90%;
    color: var(--text-gray-color);
    background: var(--text-gray-color);
  }

  &::after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 10px;
    right: 10px;
    height: 2px;
    // width: 90%;
    color: var(--text-gray-color);
    background: var(--text-gray-color);
  }

  ul {
    text-align: center;

    li {
      font-size: 70px;
    }
  }
}
</style>
