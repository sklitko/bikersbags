<template>
  <div class="grid" v-editable="blok">
    <component v-for="child in blok.columns" :key="child._uid" :blok="child" :is="child.component"></component>
  </div>
</template>

<script>
export default {
  props: ['blok']
}
</script>

<style>

</style>