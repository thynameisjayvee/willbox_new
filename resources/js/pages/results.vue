<template>
  <div class="container-fluid px-0">
    <form action="">
      <div class="extend-strip">
        <div class="container">
          test
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  metaInfo () {
    return { title: this.$t('results') }
  },

  data: () => ({
    title: window.config.appName
  }),
}
</script>

<style lang="scss" scoped>
  .extend-strip {
    position: absolute;
    top: 80px;
    min-height: 64px;
    left: 0;
    width: 100%;
    background-color: #0580FD;
    .container {
      width: 1170px;
      margin-left: auto;
      margin-right: auto;
      background-color: red;
      height: auto;
    }
  }
</style>