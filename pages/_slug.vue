<template>
  <section class="container">
    <div v-if="page.image && page.title" class="grid">
      <nuxt-picture
        v-if="page.image"
        provider="cloudinary" 
        :src="page.image" 
        fit="cropping" 
        width="600" 
        height="600" 
        class="hero"
        :modifiers="{ gravity: 'face' }"
      />
      <div class="article__heading">
        <h1 v-if="page.title">{{ page.title }}</h1>
        <p>{{ page.description }}</p>
      </div>
    </div>
    <nuxt-content :articles="articles" :document="page" />
  </section>
</template>

<script>
export default {
  async asyncData({$content, params}) {
    const page = await $content(params.slug || "index").fetch();
    const articles = await $content('articles')
        .only(['title', 'description', 'image', 'slug'])
        .sortBy('createdAt', 'desc')
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
