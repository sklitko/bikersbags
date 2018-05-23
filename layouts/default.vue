<template>
  <div>
    <Header />
    <nuxt/>
    <Footer />
  </div>
</template>

<style lang="scss">
// Customization Bootstrap vars from "app/libs/bootstrap/scss/_variables.scss"
$grid-gutter-width: 20px;
$grid-columns: 12;
$grid-breakpoints: (
  xs: 0,
  sm: 576px,
  md: 768px,
  lg: 992px,
  xl: 1200px
);
$container-max-widths: (
  sm: 540px,
  md: 720px,
  lg: 960px,
  xl: 1140px
);

$gutter: $grid-gutter-width;

$green: #2ccb77;

// @import '../node_modules/bootstrap/scss/bootstrap.scss';

// @import url(//fonts.googleapis.com/css?family=Lato:100,100italic,300,300italic,regular,italic,700,700italic,900,900italic|Libre+Baskerville:regular,italic,700|Merriweather:300,300italic,regular,italic,700,700italic,900,900italic|Montserrat:100,100italic,200,200italic,300,300italic,regular,italic,500,500italic,600,600italic,700,700italic,800,800italic,900,900italic|Open+Sans:300,300italic,regular,italic,600,600italic,700,700italic,800,800italic&subset=latin,latin-ext,vietnamese,cyrillic,devanagari,cyrillic-ext,greek-ext,greek);
body {
  background-color: #2b2c2c;
  font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
  font-size: 14px;
  color: #333;
  margin: 0;
}
</style>

