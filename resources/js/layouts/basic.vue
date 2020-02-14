<template>
  <div class="custom-container">
    <div class="custom-banner-img">
      <img src="assets/img/banner.png" alt="">
    </div>
    <div class="custom-wrapper">
      <v-navbar />
      <child />
    </div>
    <footer class="custom-footer">
      <div>
        testset foooter
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
      background-color: pink;
      padding-bottom: 60px;
    }
    &-banner-img {
      position: absolute;
      top: 0;
      left: 0;
      img {
        width: 100%;
      }
    }
    &-wrapper {
      width: 1170px;
      margin: 0 auto;
    }
    &-footer {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 60px;
      background-color: white;
    }
  }
</style>
