<template>
  <div class="custom-container">
    <div class="custom-wrapper">
      <v-navbar type="light" :nav-text-color="'black--text'" :custom-width="'w-1170-auto'" />
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
  name: 'MainLayout',

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
    &-wrapper {
      // max-width: 1170px;
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
