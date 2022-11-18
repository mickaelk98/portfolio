<script setup>

</script>

<template>
  <footer>
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
  </footer>
</template>

<style scoped lang="scss">
@import '../assets/base.scss';

footer {
  background: var(--tertiary-color);

  .container {
    position: relative;
    text-align: center;
    padding: 30px 0;
    max-width: 1300px;
    margin: auto;

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
}

@media screen and (min-width: 1024px) {
  footer {
    .container {
      display: flex;
      justify-content: space-between;
      padding: 30px 10px;

      ul {
        width: 200px;
        margin: 0;
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
  }
}
</style>
