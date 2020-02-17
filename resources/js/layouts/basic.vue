<template>
  <div class="custom-container">
    <div class="custom-banner-img">
      <img src="assets/img/banner.png" alt="banner-image">
    </div>
    <div class="custom-wrapper">
      <v-navbar />
      <child />
    </div>
    <footer class="custom-footer">
      <div class="custom-footer--text">
        ©Copyright 2020 Willbox XXXXXXXXXX
      </div>
    </footer>
  </div>
</template>

<script>
import Navbar from '~/components/Navbar'
export default {
  name: 'BasicLayout',
  components: {
    'v-navbar': Navbar
  }
}
</script>

<style lang="scss" scoped>
  .custom {
    &-container {
      min-height: 100vh;
      position: relative;
      padding-bottom: 80px;
    }
    &-banner-img {
      z-index: -1;
      position: absolute;
      top: 0;
      left: 0;
      img {
        width: 100%;
        min-height: 800px;
      }
    }
    &-wrapper {
      max-width: 1170px;
      margin: 0 auto;
    }
    &-footer {
      display: flex;
      align-items: center;
      justify-content: center;
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 80px;
      background-color: #4A4A4A;
      &--text {
        font-family: Arial, Helvetica, sans-serif;
        font-weight: bold;
        font-size: 22px;
        color: white;
      }
    }
  }
</style>
