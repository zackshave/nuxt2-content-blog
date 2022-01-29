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
      cursor: pointer;
      height: 30px;
      list-style: none;
      position: absolute;
      right: 0;
      top: 15px;
      width: 30px;

      @media screen and (min-width: 400px) {
        top: 30px
      }
      
      &.menu-icon {
        &::before {
          content: "☰";
          align-items: center;
          color: var(---text);
          display: flex;
          font-size: clamp(1.75rem, -0.875rem + 4.333vw, 2rem);
          height: 30px;
          justify-content: center;
          line-height: 1;
          padding-bottom: 8px;
          text-align: center;
          transform-origin: 15px 15px;
          transition: transform 0.2s ease;
          width: 30px;
        }
      }
    }
    
    summary::-webkit-details-marker { 
      display: none; 
    }

    &[open] {
      summary::before {
        content: "☲";
        transform: rotate(40deg);
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