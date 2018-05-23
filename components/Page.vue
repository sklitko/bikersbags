<template>
  <div v-editable="blok">
    <component v-for="child in blok.body" :key="child._uid" :products="products" :blok="child" :is="child.component"></component>
  </div>
</template>

<script>
export default {
  props: ['story', 'blok', 'products']
}
</script>

<style lang="scss">
</style>
