<template>
  <section class="container">
    <nuxt-picture
      v-if="page.image"
      provider="cloudinary" 
      :src="page.image" 
      fit="cropping" 
      width="1111" 
      height="444" 
      class="hero"
    />
    <h1>{{ page.title }}</h1>
    <nuxt-content :articles="articles" :document="page" />
  </section>
</template>

<script>
export default {
  async asyncData({$content, params}) {
    const page = await $content(params.slug || "index").fetch();
    const articles = await $content('articles')
        .only(['title', 'description', 'img', 'slug'])
        .sortBy('createdAt', 'asc')
        .fetch()
    return { 
      page: { 
        ...page, 
        articles 
      }
    }
  },
  data() {
    return {
      articles: null,
    }
  }
}
</script>
