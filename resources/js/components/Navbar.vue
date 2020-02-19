<template>
  <b-navbar toggleable="lg" :type="type" :class="['rm-box-shadow c-px-22px', customWidth]">
    <b-navbar-brand class="c-navbar-brand" :to="{ name: 'welcome' }">
      Giho
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse" />

    <b-collapse id="nav-collapse" is-nav>
      <!-- Right aligned nav items -->
      <b-navbar-nav :class="['ml-auto c-navbar-nav', navTextColor]">
        <b-nav-item class="c-mx-15px">
          Gihoとは
        </b-nav-item>
        <b-nav-item class="c-mx-15px">
          会員登録
        </b-nav-item>
        <b-nav-item class="c-mx-15px">
          ログイン
        </b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
  props: {
    type: {
      type: String,
      default: 'dark'
    },
    navTextColor: {
      type: String,
      default: 'white--text'
    },
    customWidth: {
      type: String,
      default: ''
    }
  }
}
</script>

<style lang="scss" scoped>
  .c {
    &-navbar-brand {
      font-family: Arial, Helvetica, sans-serif;
      font-size: 50px;
      font-weight: bold;
    }
    &-navbar-nav {
      color: white;
      font-family: 'Toppan Bunkyu Gothic', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      font-size: 22px;
      font-weight: 600;
      margin-right: -15px;
      &.white--text a {
        color: white  !important;
      }
      &.black--text a {
        color: #000 !important;
      }
    }
    &-px-22px {
      padding: 0 22px;
    }
    &-mx-15px {
      margin: 0 15px;
    }
  }
  .rm {
    &-box-shadow {
      box-shadow: none;
    }
  }
  .w-1170-auto {
    max-width: 1170px;
    margin-left: auto;
    margin-right: auto;
  }
</style>
