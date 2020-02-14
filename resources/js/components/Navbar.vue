<template>
  <b-navbar toggleable="lg" type="dark" class="rm-box-shadow c-px-32px">
    <b-navbar-brand class="c-navbar-brand" href="#">
      Giho
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse" />

    <b-collapse id="nav-collapse" is-nav>
      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto c-navbar-nav">
        <b-navbar-item class="c-mx-15px">
          Gihoとは
        </b-navbar-item>
        <b-navbar-item class="c-mx-15px">
          会員登録
        </b-navbar-item>
        <b-navbar-item class="c-mx-15px">
          ログイン
        </b-navbar-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
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
    }
    &-px-32px {
      padding: 0 32px;
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
</style>
