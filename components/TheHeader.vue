<template>
  <header>
    <nav>
      <h1 v-if="$route.path === '/'" class="logo unicode-title">
        <span class="visually-hidden">Welcome to zackshave.dev</span>
      </h1>
      <NuxtLink v-else to="/" class="logo unicode-title"><span class="visually-hidden">Home</span></NuxtLink>
    </nav>
  </header>
</template>

<style scoped lang="scss">
  h1 {
    font-family: unset;
  }

  a {
    font-weight: 200;

    &:hover, &:active, &:focus {
      color: var(---accent);

      &::before {
        background-color: transparent;
      }
    }
  }

  .logo {
    color: var(---text);
    display: inline-block;
    margin-bottom: 32px;
    transition: color 0.25s ease;
  }  

  .unicode-title {
    position: relative;

    &::after {
      content: var(---logo);
      font-size: clamp(2.25rem, -0.875rem + 12.333vw, 3.5rem);
      font-weight: 200;
      letter-spacing: 1px;
    }
  }
</style>