<template>
  <div v-editable="blok">
    <h2>{{blok.name}}</h2>
    <component v-for="child in blok.body" :key="child._uid" :blok="child" :is="child.component"></component>
  </div>
</template>

<script>
export default {
  props: ['story', 'blok']
}
</script>