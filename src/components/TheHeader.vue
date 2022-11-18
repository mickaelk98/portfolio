<script setup>

</script>

<template>
  <header>
    <div class="container">
      <!-- nom -->
      <h2>Mickael Keita</h2>

      <!-- reseaux saciaux -->
      <ul>
        <li>
          <a href="https://github.com/mickaelk98" target="_blank"><i class="fa-brands fa-github"></i></a>
        </li>
        <li>
          <a href="https://www.linkedin.com/in/mickael-keita/" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
        </li>
      </ul>
    </div>
  </header>
</template>

<style scoped lang="scss">
@import '../assets/base.scss';

header {
  background: var(--secondary-color);

  .container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px 10px;
    margin: auto;
    max-width: 1300px;

    ul {
      width: 20%;
      color: var(--text-color);
      display: flex;
      align-content: center;
      justify-content: space-between;
      max-width: 200px;

      li i {
        font-size: 22px;
        transition: transform 0.3s;

        &:hover {
          cursor: pointer;
          transform: scale(1.2);
        }
      }
    }
  }
}

@media screen and (min-width: 1024px) {
  header {
    .container {
      padding: 20px 10px;
    }
  }
}
</style>
