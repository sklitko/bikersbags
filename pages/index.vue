<template>
  <div>
    <Header :transparentNavbar="story.content.transparent_navbar" />
    <component v-if="story.content.component" :key="story.content._uid" :story="story" :products="products" :blok="story.content" :is="story.content.component"></component>
  </div>
</template>

<script>
export default {
  async asyncData(context) {
    let [storyRes, productRes] = await Promise.all([
      context.app.$storyapi.get('cdn/stories/home', { version: 'draft' }),
      context.app.$storyapi.get('cdn/stories', {
        version: 'draft',
        starts_with: 'products/'
      })
    ])
    return {
      story: storyRes.data.story,
      products: productRes.data.stories
    }
  }
}
</script>


<style lang="scss">
</style>
