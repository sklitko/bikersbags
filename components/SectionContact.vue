<template>
  <div v-editable="blok" class="section-contact">
    <div class="container-fluid">
      <div class="row">
        <div class="col-12 col-sm-4">
          <h2>{{blok.title}}</h2>
          <div class="divider">
            <hr>
          </div>
          <component v-for="child in blok.body" :key="child._uid" :blok="child" :is="child.component"></component>
        </div>
        <div class="col-12 col-sm-8 mt-3 mt-sm-0">
          <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d10579.982849004573!2d35.165536867163105!3d48.47579584935983!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sru!2sua!4v1522841220076" width="100%" height="380px" frameborder="0" style="border:0" allowfullscreen=""></iframe>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  props: ['story', 'blok']
}
</script>


<style lang="scss">
.section-contact {
  padding-bottom: 170px;
  padding-top: 170px;
  background-color: #212121;
  h2 {
    font-weight: 400;
    font-style: normal;
    font-family: 'Montserrat', sans-serif;
    color: #ffffff;
    font-size: 39px;
    line-height: 1.2;
    letter-spacing: 0px;
    text-transform: uppercase;
    margin-bottom: 0;
  }
  .divider {
    text-align: left;
  }
}
</style>
