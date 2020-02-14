<template>
  <div>
    <div class="c-search-box">
      <h1 class="c-search-title">
        Direct Matching Logistics Platform
      </h1>
      <div class="c-search-card">
        <b-tabs content-class="mt-3" nav-class="c-search-tabs rm-border-bot" active-nav-item-class="c-search-tabs--active">
          <b-tab active>
            <template #title>
              <div class="c-search-tabs-title">
                <img src="assets/img/car.png" alt="car-icon">
                <span style="vertical-align: middle;">トラック</span>
              </div>
            </template>
            <form action="" style="margin-top: 30px;">
              <b-form-row>
                <b-col cols="12">
                  <b-form-input
                    id="input-1"
                    type="text"
                    required
                    placeholder="特定業者を検索"
                    class="c-search-input supplier"
                  />
                </b-col>
                <h2 class="c-search-form-title">
                  基本情報
                </h2>
              </b-form-row>
            </form>
          </b-tab>
          <b-tab>
            <template #title>
              <div class="c-search-tabs-title">
                <img src="assets/img/package.png" alt="package-icon">
                <span style="vertical-align: middle;">梱包</span>
              </div>
            </template>
            <p>I'm the 2nd tab</p>
          </b-tab>
          <b-tab>
            <template #title>
              <div class="c-search-tabs-title">
                <img src="assets/img/notes.png" alt="notes-icon">
                <span style="vertical-align: middle;">通関</span>
              </div>
            </template>
            <p>I'm the 3rd tab</p>
          </b-tab>
          <b-tab>
            <template #title>
              <div class="c-search-tabs-title">
                <img src="assets/img/warehouse.png" alt="warehouse-icon">
                <span style="vertical-align: middle;">通関</span>
              </div>
            </template>
            <p>I'm the 4th tab</p>
          </b-tab>
        </b-tabs>
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  layout: 'basic',

  metaInfo () {
    return { title: this.$t('home') }
  },

  data: () => ({
    title: window.config.appName
  }),

  computed: mapGetters({
    authenticated: 'auth/check'
  })
}
</script>

<style lang="scss" scoped>
  ::v-deep {
    .c {
      &-search {
        &-box {
          margin: 135px 106px 0 106px;
        }
        &-title {
          font-family: Arial, Helvetica, sans-serif;
          font-size: 44px;
          font-weight: bold;
          color: white;
          text-align: center;
        }
        &-card {
          background-color: white;
          padding: 20px;
          margin-top: 30px;
        }
        &-form-title {
          font-family: 'Hiragino Kaku Gothic Pro', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
          font-size: 18px;
          font-weight: 600;
          color: #6E6E6E;
          margin-top: 35px;
          padding: 0 5px;
        }
        &-input {
          font-family: 'Hiragino Kaku Gothic Pro', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
          font-size: 16px;
          font-weight: 300;
          color: #6E6E6E;
          &.supplier {
            width: 67.3%;
            height: 60px;
            background-color: #EBEBEB;
          }
        }
        &-tabs {
          .nav-link {
            padding: 4px 8px;
            height: 100%;
            border-bottom: 1px solid #C3C3C3;
          }
          li:not(:last-child) {
            margin-right: 70px;
          }
          &-title {
            color: #7B7B7B;
            font-family: 'Hiragino Kaku Gothic Pro', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            font-size: 18px;
            font-weight: 300;
            height: 100%;
          }
          &--active {
            color: #7B7B7B !important;
            background-color: transparent !important;
            border-color: transparent !important;
            border-bottom: 2px solid #116ED6 !important;
            position: relative;
            &:after {
              content: url(/assets/img/blue-arr.png); /* with class ModalCarrot ??*/
              position: absolute; /*or absolute*/
              margin-top: 5%;
              left: 50%;
              transform: translateX(-50%);
            }
          }
        }
      }
    }
    .rm {
      &-border {
        &-bot {
          border-bottom: none;
        }
      }
    }
  }
</style>
