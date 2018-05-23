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
        dersion: 'draft'
      })
      .then(res => {
        return {
          productItems: res.data.story.content.productItems,
          transparentNavbar: res.data.story.content.transparent_navbar
        }
      })
  }
}
</script>
