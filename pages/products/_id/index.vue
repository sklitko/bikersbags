<template>
  <div>
    <Header :transparentNavbar="transparentNavbar" />
    <main class="section-content">
      <div class="grid">
        <component v-for="productItem in productItems" :key="productItem._uid" :blok="productItem" :is="productItem.component"></component>
      </div>

    </main>
  </div>
</template>

<script>
export default {
  asyncData(context) {
    return context.app.$storyapi
      .get('cdn/stories/products/' + context.params.id, {
        version: process.env.NODE_ENV == 'production' ? 'published' : 'draft'
      })
      .then(res => {
        return {
          productItems: res.data.story.content.productItems,
          transparentNavbar: res.data.story.content.transparent_navbar
        }
      })
  },
  mounted() {
    this.$storyblok.init()
  }
}
</script>
