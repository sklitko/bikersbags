<template>
  <div v-editable="blok" class="section-price">
    <div class="container-fluid">
      <div class="row">
        <div class="col-12">
          <h2>{{blok.title}}</h2>
          <div class="divider">
            <hr>
          </div>
        </div>
      </div>
      <div class="row">
        <component v-for="child in products" :key="child._uid" :blok="child" :is="child.content.component"></component>

      </div>
    </div>

  </div>
</template>

<script>
export default {
  props: ['products', 'blok']
}
</script>


<style lang="scss">
.container-fluid {
  max-width: 1200px;
}

.divider {
  padding: 25px 0;
  text-align: center;
  line-height: 0;
  hr {
    width: 20%;
    border-top-width: 2px;
    border-top-style: solid;
    border-top-color: #2ccb77;
    margin: 0;
    display: inline-block;
  }
}

.section-price {
  background-color: #2b2c2c;
  padding-bottom: 170px;
  padding-top: 170px;
  .divider {
    padding: 25px 0 40px;
    hr {
      width: 10%;
    }
  }
  h2 {
    font-weight: 400;
    font-style: normal;
    font-family: Montserrat, sans-serif;
    color: #fff;
    font-size: 39px;
    line-height: 1.2;
    letter-spacing: 0;
    text-transform: uppercase;
    margin-bottom: 0;
    text-align: center;
  }
}
</style>
