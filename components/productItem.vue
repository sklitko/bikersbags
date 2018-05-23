<template>

  <div class="grid-item">
    <div class="item" :style="{backgroundImage: 'url(' + blok.image_1 + ')'}"></div>
    <div class="item" :style="{backgroundImage: 'url(' + blok.image_2 + ')'}"></div>
    <div class="item" :style="{backgroundImage: 'url(' + blok.image_3 + ')'}"></div>
    <div class="item" :style="{backgroundImage: 'url(' + blok.image_4 + ')'}"></div>
  </div>

</template>

<script>
export default {
  props: ['blok']
}
</script>
