<template>
  <main class="section-content">
    <component v-for="productItem in productItems" :key="productItem._uid" :blok="productItem" :is="productItem.component"></component>
  </main>
</template>

<script>
export default {
  asyncData(context) {
    return context.app.$storyapi
      .get('cdn/stories/products/' + context.params.id, {
        dersion: 'draft'
      })
      .then(res => {
        return { productItems: res.data.story.content.productItems }
      })
  }
}
</script>
