<template>
  <div class="section-hero" :style="{backgroundImage: 'url('+blok.image+')'}">
    <div class="container-fluid">
      <div class="row">
        <div class="col">
          <h1>{{blok.headline}}</h1>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  props: ['blok']
}
</script>


<style lang="scss">
.section-hero {
  background-position: center top;
  background-repeat: no-repeat;
  background-size: cover;
  height: 95vh;
  padding-top: 150px;
  padding-bottom: 150px;
  h1 {
    transition: 0.3s;
    font-weight: 400;
    color: #fff;
    font-size: 60px;
    line-height: 1.2;
    font-family: 'Montserrat', sans-serif;
    padding-top: 200px;
    padding-bottom: 220px;
  }
}
</style>
