<template>
  <article>
    <div class="grid">
      <div class="article__image">
        <nuxt-picture
          v-if="article.img"
          provider="cloudinary" 
          :src="article.img" 
          fit="cropping" 
          width="600" 
          height="600" 
          alt="article.alt"
        />
        <small>Article last updated: {{ formatDate(article.updatedAt) }}</small>
      </div>
      <div class="article__heading">
        <h1>{{ article.title }}</h1>
        <p>{{ article.description }}</p>
      </div>
    </div>
    <nuxt-content :document="article" />
  </article>
</template>

<script>
  export default {
    async asyncData({ $content, params }) {
      const article = await $content('articles', params.slug).fetch()

      return { article }
    },
    methods: {
      formatDate(date) {
        const options = { year: 'numeric', month: 'long', day: 'numeric' }
        return new Date(date).toLocaleDateString('en', options)
      }
    }
  }
</script>
