<template>
  <header>
    <nav>
      <NuxtLink to="/" class="logo unicode-title"><span class="visually-hidden">Home</span></NuxtLink>
      <TheMainMenu />
    </nav>
  </header>
</template>

<style scoped lang="scss">
  header {
    margin-bottom: 32px;
  }

  .logo {
    color: var(---text);
    display: block;
    margin-bottom: 32px;
    transition: color 0.25s ease;

    &:hover, &:active, &:focus {
      color: var(---accent);
    }
  }  

  .unicode-title {
    &::after {
      content: var(---logo);
      font-size: clamp(2.25rem, -0.875rem + 12.333vw, 3.5rem);
      font-weight: 200;
      letter-spacing: 1px;
    }
  }
</style>