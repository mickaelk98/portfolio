<script setup>

</script>

<template>
  <footer>
    <!-- nom -->
    <h2>Mickael Keita</h2>

    <!-- reseaux saciaux -->
    <ul>
      <li>
        <a href="https://github.com/mickaelk98" target="_blank"><i class="fa-brands fa-github"></i></a>
      </li>
      <li>
        <a href="https://www.linkedin.com/in/mickael-keita/"><i class="fa-brands fa-linkedin"></i></a>
      </li>
    </ul>
  </footer>
</template>

<style scoped lang="scss">
@import '../assets/base.scss';

footer {
  position: relative;
  background: var(--secondary-color);
  text-align: center;
  padding: 30px 0;

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

  h2 {
    margin-bottom: 20px;
  }

  ul {
    width: 20%;
    margin: auto;
    display: flex;
    justify-content: space-between;

    li {
      color: var(--text-color);
      font-size: 22px;
      cursor: pointer;
      transition: transform 0.3s;

      &:hover {
        transform: scale(1.2);
      }
    }
  }
}
</style>
