<template>
  <footer>
    <p><NuxtLink to="/" class="logo unicode-title"><span class="visually-hidden">Home</span></NuxtLink></p>
    <p>©{{ new Date().getFullYear() }}</p>
  </footer>
</template>

<style scoped lang="scss">
  footer {
    text-align: center;
  }

  .logo {
    color: var(---text);
    display: inline-block;
    transition: color 0.25s ease;

    &:hover, &:active, &:focus {
      color: var(---accent);
    }
  }  

  .unicode-title {
    &::before {
      content: var(---logo);
      font-size: 20px;
      letter-spacing: 1px;
    }
  }
</style>