<template>
  <header class="section-header" :class="{ 'items' : !transparentNavbar}">

    <div class="container-fluid">
      <nav class="navbar navbar-expand-md py-3">

        <logo />

        <!-- <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button> -->
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav ml-auto align-baseline">
            <li class="nav-item active">
              <a class="nav-link link-active" href="#">Home
              </a>
            </li>

            <!-- <li class="nav-item">
              <a class="nav-link" href="#">Price list</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Portfolio</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Contacts</a>
            </li> -->
            <li class="nav-item">
              <a class="nav-link" href="#">Language</a>
            </li>
          </ul>
        </div>
      </nav>

    </div>
  </header>
</template>


<script>
export default {
  props: ['transparentNavbar']
}
</script>

<style lang="scss">
.section-header {
  position: absolute;
  width: 100%;
  .logo {
    height: 150px;
  }
}

.section-header.items {
  background-image: none;
  background-image: none;
  position: relative;
}

.navbar {
  .nav-item {
    &:not(:first-child) {
      margin-left: 29px;
    }

    &:hover {
      .nav-link {
        color: #2ccb77;
        border-color: #2ccb77;
      }
    }

    .nav-link {
      color: #fff;
      text-decoration: none;
      font-family: 'Montserrat', sans-serif;
      font-weight: 300;
      line-height: 21px;
      padding-bottom: 5px;
      border-bottom: 2px solid transparent;
      letter-spacing: 1.2px;
      font-size: 12px;
      transition: 0.3s;
      text-align: left;
      text-transform: uppercase;
      font-style: normal;
      &.link-active {
        color: #fff;
        border-bottom: 2px solid #2ccb77;
      }
    }
  }
}
</style>
