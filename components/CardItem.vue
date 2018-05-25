<template>
  <div class="col-12 col-md-4 mb-3">
    <div class="card" v-editable="blok">
      <img :src="blok.content.image" alt="" class="card-img-top">
      <div class="card-body">
        <h5 class="card-title">{{blok.content.title}}</h5>
        <p class="card-price">${{blok.content.price}}</p>
        <div class="divider">
          <hr>
        </div>
        <p class="card-text">{{blok.content.text}}</p>
        <nuxt-link :to="blok.full_slug" class="btn btn-primary">{{blok.content.text_button}}</nuxt-link>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  props: ['blok'],
  mounted() {
    this.$storyblok.init()
  }
}
</script>

<style lang="scss">
.card {
  background-color: #212121;
  border-radius: 0;
  .card-body {
    text-align: center;
    padding: 0;
    padding-top: 1.25rem;
  }
  .card-img-top {
    border-radius: 0;
  }
  .card-title {
    text-align: center;
    transition: 0.3s;
    font-size: 16px;
    line-height: 1.9;
    font-weight: 400;
    color: #2ccb77;
    font-family: 'Montserrat', sans-serif;
    margin-bottom: 0;
  }

  .card-price {
    text-align: center;
    transition: 0.3s;
    font-weight: 300;
    color: #ffffff;
    font-size: 46px;
    line-height: 1.4;
    font-family: 'Montserrat', sans-serif;
    margin-bottom: 0;
  }

  .card-text {
    text-align: center;
    transition: 0.3s;
    font-weight: 400;
    font-style: normal;
    font-family: 'Open Sans', sans-serif;
    color: #a2a2a2;
    font-size: 16px;
    line-height: 1.7;
    margin-bottom: 0;
    padding-left: 60px;
    padding-right: 60px;
    padding-bottom: 25px;
  }

  .btn-primary {
    font-family: 'Montserrat', sans-serif;
    font-weight: 300;
    font-style: normal;
    color: #ffffff;
    background-color: #2ccb77;
    font-size: 12px;
    padding: 17px 15px;
    min-width: 180px;
    position: relative;
    text-align: center;
    z-index: 1;
    transition: 0.3s;
    line-height: 22px;
    border: 2px solid #2ccb77;
    border-radius: 3px;
    letter-spacing: 1.2px;
    margin-bottom: 60px;
    text-transform: uppercase;
  }
}
</style>

