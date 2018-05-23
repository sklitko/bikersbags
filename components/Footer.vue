<template>
  <footer>
    <div class="footer-logo mb-4">
      <logo />
    </div>
    <ul class="social-links">
      <li class="social-links-item">

        <a href="#" class="social-links-link facebook">
          <font-awesome-icon :icon="['fab', 'facebook-f']" />
        </a>
      </li>
      <li class="social-links-item">
        <a href="#" class="social-links-link twitter">
          <font-awesome-icon :icon="['fab', 'twitter']" />
        </a>
      </li>
      <li class="social-links-item">
        <a href="#" class="social-links-link">
          <font-awesome-icon :icon="['fab', 'instagram']" />
        </a>
      </li>
      <li class="social-links-item">
        <a href="#" class="social-links-link">
          <font-awesome-icon :icon="['fab', 'google-plus-g']" />
        </a>
      </li>
    </ul>
    <p class="copyright">© Copyrights 2018 Horsepower. All Right Reserved. Developed By Klitko</p>
  </footer>
</template>

<script>
export default {}
</script>

<style lang="scss">
footer {
  padding: 50px 0;
  background-color: #140b05;
  text-align: center;
  .social-links {
    margin-bottom: 25px;
    list-style: none;
    // margin: 0;gu

    padding: 0;
    display: inline-block;
    .social-links-item {
      display: inline-block;
      list-style: none;
      .social-links-link {
        width: 60px;
        height: 60px;
        line-height: 60px;
        font-size: 26px;
        border-radius: 50%;
        border: none;
        margin: 0 15px;
        display: inline-block;
        text-align: center;
        position: relative;
        transition: all 0.3s ease;
        color: #2ccb77;
        transition: 0.3s;
        &:hover {
          background-color: #2ccb77;
          color: #140b05;
        }
      }
    }
  }

  .footer-logo {
    img {
      height: 100px;
    }
  }

  .copyright {
    font-weight: 400;
    font-style: normal;
    font-family: 'Open Sans', sans-serif;
    color: #a69fa5;
    font-size: 16px;
    line-height: 1.6;
    letter-spacing: 0px;
  }
}
</style>

