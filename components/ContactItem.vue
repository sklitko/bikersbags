<template>
  <div class="item-contact" v-editable="blok">
    <h5>{{blok.title}}</h5>
    <p>{{blok.text}}</p>
  </div>
</template>

<script>
export default {
  props: ['blok']
}
</script>

<style lang="scss">
.item-contact {
  padding-top: 25px;
  h5 {
    font-weight: 400;
    font-style: normal;
    font-family: 'Montserrat', sans-serif;
    color: #2ccb77;
    font-size: 16px;
    line-height: 1.9;
    letter-spacing: 0px;
    margin: 0;
  }
  p {
    font-weight: 400;
    font-style: normal;
    font-family: 'Open Sans', sans-serif;
    color: #dbdbdb;
    font-size: 16px;
    line-height: 1.7;
    letter-spacing: 0px;
    margin: 0;
  }
}
</style>

