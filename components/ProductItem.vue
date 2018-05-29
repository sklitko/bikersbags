<template>

  <div class="grid-item" v-editable="blok">
    <div class="item" :style="{backgroundImage: 'url(' + blok.image_1 + ')'}"></div>
    <div class="item" :style="{backgroundImage: 'url(' + blok.image_2 + ')'}"></div>
    <div class="item" :style="{backgroundImage: 'url(' + blok.image_3 + ')'}"></div>
    <div class="item" :style="{backgroundImage: 'url(' + blok.image_4 + ')'}"></div>
    <button class="button-link" @click="showModal = true">Заказать</button>
    <modal v-if="showModal" @close="showModal = false">

    </modal>
  </div>

</template>

<script>
export default {
  props: ['blok'],
  data: () => ({
    showModal: false
  }),
  mounted() {
    this.$storyblok.init()
  }
}
</script>


<style lang="scss">
.button-link {
  font-family: 'Montserrat', sans-serif;
  font-weight: 300;
  font-style: normal;
  color: #ffffff;
  background-color: #2ccb77;
  border-color: #2ccb77;
  position: absolute;
  font-size: 12px;
  padding: 17px 15px;
  min-width: 180px;
  text-align: center;
  transition: 0.3s;
  border-radius: 3px;
  top: calc(50% - 25px);
  left: calc(50% - 90px);
  z-index: 1;
  visibility: hidden;
  text-transform: uppercase;
  text-decoration: none;
  &:hover {
    color: #ffffff;
    background-color: #a2a2a2;
    border-color: #a2a2a2;
    text-decoration: none;
  }
}

.grid-item:hover {
  .button-link {
    visibility: visible;
  }
}
</style>
