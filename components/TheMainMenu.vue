<template>
  <details>
    <summary class="menu-icon"><span class="visually-hidden">Menu</span></summary>
    <nav>
      <ul>
        <li><NuxtLink to="/">Home</NuxtLink></li>
        <li><NuxtLink to="/about">About</NuxtLink></li>
        <li><NuxtLink to="/contact">Contact</NuxtLink></li>
      </ul>
    </nav>
  </details>
</template>

<style scoped lang="scss">
  details {

    summary {
      align-items: center;
      cursor: pointer;
      display: flex;
      height: 30px;
      justify-content: center;
      list-style: none;
      position: absolute;
      right: 0;
      text-align: center;
      top: 15px;
      transform-origin: 15px 15px;
      transition: transform 0.2s ease;
      width: 30px;

      @media screen and (min-width: 600px) {
        height: 35px;
        top: 30px;
        width: 35px;
      }
      
      &.menu-icon {
        &::before {
          content: "☰";
          color: var(---text);
          font-size: clamp(1.25rem, -0.875rem + 4.333vw, 1.5rem);
          line-height: 1;
          padding: 0 0 5px 0;
          text-align: center;
        }
      }
    }
    
    summary::-webkit-details-marker { 
      display: none; 
    }

    &[open] {
      summary {
        transform: rotate(45deg);

        &::before {
          content: "☲";
        }
      }
    }

    nav {
      background-color: var(---background);
      margin-top: 8px;;
    }
    
    ul {
      display: flex;
      flex-flow: row nowrap;
      list-style: none;
      margin: 0;
      padding: 0;

      li {
        margin-right: 16px;

        a {
          font-size: clamp(0.75rem, -0.875rem + 4.333vw, 1rem);
          font-weight: 400;

          &.nuxt-link-exact-active {
            text-decoration: underline;
          }
        }
      }
    }
  }
</style>