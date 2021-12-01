<template>
  <div>
    <ul class="scroll-grid">
      <li v-for="article of articles" :key="article.slug">
        <article v-if="article.image">
          <h3>
            <NuxtLink :to="{ name: 'blog-slug', params: { slug: article.slug } }">{{ article.title }}</NuxtLink>
          </h3>
          <nuxt-picture
            v-if="article.image"
            provider="cloudinary" 
            :src="article.image" 
            fit="cropping" 
            width="1000" 
            height="1000"
            alt="article.alt"
          />
        </article>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    props: {
      articles: {
        type: Array,
        default: null
      }
    }
  }
</script>

<style scoped lang="scss">
  ul {
    list-style: none;
    margin: 32px 0;
    padding: 0;

    li {
      article {
        position: relative;

        a {
          align-items: center;
          display: flex;
          gap: 5px;
          text-decoration: none;

          &::before {
            bottom: 0;
            content: '';
            height: 100%;
            left: 0;
            position: absolute;
            right: 0;
            top: 0;
          }

          &::after {
            content: "→";
          }
        }
      }
    }
  }
</style>