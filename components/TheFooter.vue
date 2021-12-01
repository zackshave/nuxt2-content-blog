<template>
  <footer>
    <hr>
    <p v-if="$route.path === '/'" class="logo unicode-title"><span class="visually-hidden">Home</span></p>
    <p v-else><NuxtLink to="/" class="logo unicode-title"><span class="visually-hidden">Home</span></NuxtLink></p>
    <p>©{{ new Date().getFullYear() }}</p>
  </footer>
</template>

<style scoped lang="scss">
  footer {
    margin-top: 32px;
    text-align: center;
  }

  p {
    margin: 0 0 8px 0;
  }

  a {
    &:hover, &:active, &:focus {
      color: var(---accent);
    }
  }

  .logo {
    color: var(---text);
    display: inline-block;
    transition: color 0.25s ease;
  }  

  .unicode-title {
    &::before {
      content: var(---logo);
      font-size: 20px;
      letter-spacing: 1px;
    }
  }
</style>