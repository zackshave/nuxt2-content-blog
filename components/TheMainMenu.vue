<template>
  <ul class="main-menu">
    <li class="main-menu__item">
      <NuxtLink to="/about">About</NuxtLink>
    </li>
    <li class="main-menu__item">
      <NuxtLink to="/contact">Contact</NuxtLink>
    </li>
  </ul>
</template>

<style scoped lang="scss">
  ul {
    display: flex;
    list-style: none;
    padding: 0;

    li {
      margin-right: 16px;

      a {
        font-size: clamp(1rem, -0.875rem + 4.333vw, 1.125rem);
        font-weight: 400;
      }
    }
  }
</style>