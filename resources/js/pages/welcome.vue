<template>
  <div class="container-fluid px-0">
    <!-- start of search box -->
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
            <!-- FORM START -->
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
                <h2 class="c-search-form-title w-100">
                  基本情報
                </h2>
                <b-row class="no-gutters w-100 c-mx-5px">
                  <b-col cols="12" md="3">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="搬入港を選択してください"
                    />
                  </b-col>
                  <b-col cols="12" md="3">
                    <custom-datepicker v-model="date" class="rm-mx-calendar-icon w-100" input-class="form-control c-search-input w-arr" :clearable="false" />
                  </b-col>
                  <b-col cols="12" md="3">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="出発地を入力してください"
                    />
                  </b-col>
                  <b-col cols="12" md="3">
                    <b-form-select v-model="selected" :options="options" class="c-search-input" />
                  </b-col>
                </b-row>
                <h2 class="c-search-form-title w-100">
                  製品情報
                </h2>
                <b-row class="no-gutters w-100 c-mx-5px">
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="長さ(L) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="幅(W) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="高さ(H) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="製品重量 kg"
                    />
                  </b-col>
                  <b-col cols="12" md="2" class="d-flex align-items-center justify-content-center">
                    <b-form-checkbox-group
                      class="c-search-checkbox"
                      :options="[{ text: '引取り', value: '引取り' },
                                 { text: '保険希望', value: '保険希望' },
                      ]"
                      name="flavour-2a"
                      stacked
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-button variant="primary" squared class="c-search-btn float-md-right" :to="{ name: 'results' }">
                      検索
                    </b-button>
                  </b-col>
                </b-row>
              </b-form-row>
            </form>
            <!-- FORM END -->
          </b-tab>
          <b-tab>
            <template #title>
              <div class="c-search-tabs-title">
                <img src="assets/img/package.png" alt="package-icon">
                <span style="vertical-align: middle;">梱包</span>
              </div>
            </template>
            <!-- FORM START -->
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
                <h2 class="c-search-form-title w-100">
                  基本情報
                </h2>
                <b-row class="no-gutters w-100 c-mx-5px">
                  <b-col cols="12" md="3">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="搬入港を選択してください"
                    />
                  </b-col>
                  <b-col cols="12" md="3">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="CYカット日"
                    />
                  </b-col>
                  <b-col cols="12" md="3">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="出発地を入力してください"
                    />
                  </b-col>
                  <b-col cols="12" md="3">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="梱包仕様を選択してください"
                    />
                  </b-col>
                </b-row>
                <h2 class="c-search-form-title w-100">
                  製品情報
                </h2>
                <b-row class="no-gutters w-100 c-mx-5px">
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="長さ(L) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="幅(W) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="高さ(H) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="製品重量 kg"
                    />
                  </b-col>
                  <b-col cols="12" md="2" class="d-flex align-items-center justify-content-center">
                    <b-form-checkbox-group
                      class="c-search-checkbox"
                      :options="[{ text: '引取り', value: '引取り' },
                                 { text: '保険希望', value: '保険希望' },
                      ]"
                      name="flavour-2a"
                      stacked
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-button variant="primary" squared class="c-search-btn float-md-right">
                      検索
                    </b-button>
                  </b-col>
                </b-row>
              </b-form-row>
            </form>
            <!-- FORM END -->
          </b-tab>
          <b-tab>
            <template #title>
              <div class="c-search-tabs-title">
                <img src="assets/img/notes.png" alt="notes-icon">
                <span style="vertical-align: middle;">通関</span>
              </div>
            </template>
            <!-- FORM START -->
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
                <h2 class="c-search-form-title w-100">
                  基本情報
                </h2>
                <b-row class="no-gutters w-100 c-mx-5px">
                  <b-col cols="12" md="3">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="搬入港を選択してください"
                    />
                  </b-col>
                  <b-col cols="12" md="3">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="CYカット日"
                    />
                  </b-col>
                  <b-col cols="12" md="3">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="出発地を入力してください"
                    />
                  </b-col>
                  <b-col cols="12" md="3">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="梱包仕様を選択してください"
                    />
                  </b-col>
                </b-row>
                <h2 class="c-search-form-title w-100">
                  製品情報
                </h2>
                <b-row class="no-gutters w-100 c-mx-5px">
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="長さ(L) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="幅(W) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="高さ(H) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="製品重量 kg"
                    />
                  </b-col>
                  <b-col cols="12" md="2" class="d-flex align-items-center justify-content-center">
                    <b-form-checkbox-group
                      class="c-search-checkbox"
                      :options="[{ text: '引取り', value: '引取り' },
                                 { text: '保険希望', value: '保険希望' },
                      ]"
                      name="flavour-2a"
                      stacked
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-button variant="primary" squared class="c-search-btn float-md-right">
                      検索
                    </b-button>
                  </b-col>
                </b-row>
              </b-form-row>
            </form>
            <!-- FORM END -->
          </b-tab>
          <b-tab>
            <template #title>
              <div class="c-search-tabs-title">
                <img src="assets/img/warehouse.png" alt="warehouse-icon">
                <span style="vertical-align: middle;">倉庫</span>
              </div>
            </template>
            <!-- FORM START -->
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
                <h2 class="c-search-form-title w-100">
                  基本情報
                </h2>
                <b-row class="no-gutters w-100 c-mx-5px">
                  <b-col cols="12" md="3">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="搬入港を選択してください"
                    />
                  </b-col>
                  <b-col cols="12" md="3">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="CYカット日"
                    />
                  </b-col>
                  <b-col cols="12" md="3">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="出発地を入力してください"
                    />
                  </b-col>
                  <b-col cols="12" md="3">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="梱包仕様を選択してください"
                    />
                  </b-col>
                </b-row>
                <h2 class="c-search-form-title w-100">
                  製品情報
                </h2>
                <b-row class="no-gutters w-100 c-mx-5px">
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="長さ(L) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="幅(W) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="高さ(H) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="c-search-input w-arr"
                      placeholder="製品重量 kg"
                    />
                  </b-col>
                  <b-col cols="12" md="2" class="d-flex align-items-center justify-content-center">
                    <b-form-checkbox-group
                      class="c-search-checkbox"
                      :options="[{ text: '引取り', value: '引取り' },
                                 { text: '保険希望', value: '保険希望' },
                      ]"
                      name="flavour-2a"
                      stacked
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-button variant="primary" squared class="c-search-btn float-md-right">
                      検索
                    </b-button>
                  </b-col>
                </b-row>
              </b-form-row>
            </form>
            <!-- FORM END -->
          </b-tab>
        </b-tabs>
      </div>
    </div>
    <!-- end of search box -->
    <!-- start of services box -->
    <div class="c-services-box">
      <h1 class="c-services-title">
        Gihoとは
      </h1>
      <b-row>
        <b-col cols="12" md="4" class="text-center">
          <div class="c-services-img d-flex justify-content-center">
            <img src="assets/img/community.png" alt="community-icon">
          </div>
          <h2 class="c-services-sub-title">
            高いお客さま満足度
          </h2>
          <p class="c-services-text-content">
            ○〇〇○〇〇○〇〇○〇〇○〇〇○〇〇
            〇○〇〇○〇〇〇○〇〇○〇〇
          </p>
        </b-col>
        <b-col cols="12" md="4" class="text-center">
          <div class="c-services-img d-flex justify-content-center">
            <img src="assets/img/handshake.png" alt="handshake-icon">
          </div>
          <h2 class="c-services-sub-title">
            業界初ダイレクトマッチング
          </h2>
          <p class="c-services-text-content">
            ○〇〇○〇〇○〇〇○〇〇○〇〇○〇〇
            〇○〇〇○〇〇〇○〇〇○〇〇
          </p>
        </b-col>
        <b-col cols="12" md="4" class="text-center">
          <div class="c-services-img d-flex justify-content-center">
            <img src="assets/img/gear.png" alt="gear-icon">
          </div>
          <h2 class="c-services-sub-title">
            スムーズなプラン選定
          </h2>
          <p class="c-services-text-content">
            ○〇〇○〇〇○〇〇○〇〇○〇〇○〇〇
            〇○〇〇○〇〇〇○〇〇○〇〇
          </p>
        </b-col>
      </b-row>
    </div>
    <!-- end of services-box -->
    <!-- start of products-box -->
    <div class="c-products-box">
      <h1 class="c-products-title text-center">
        Gihoとは
      </h1>
      <b-row>
        <b-col
          v-for="index in 6"
          :key="index"
          cols="12"
          md="6"
          class="mb-4"
        >
          <div class="c-card">
            <b-row>
              <b-col cols="12" md="6">
                <div class="title">
                  株式会社○○○○
                </div>
              </b-col>
              <b-col cols="12" md="6">
                <b-button variant="primary" squared class="title btn ml-md-auto">
                  このベンダーで検索
                </b-button>
              </b-col>
              <b-col cols="12" class="mt-1 d-flex">
                <div class="mr-md-3">
                  <star-rating
                    :star-size="24"
                    rating="4"
                    :padding="8"
                    read-only
                    :show-rating="false"
                    border-color="#ffd055"
                  />
                </div>
                <span class="item-text">126件</span>
              </b-col>
              <b-col cols="12" class="d-flex mt-3">
                <div class="chips">
                  トラック
                </div>
                <div class="chips">
                  梱包
                </div>
                <div class="chips">
                  倉庫保管
                </div>
              </b-col>
            </b-row>
          </div>
        </b-col>
      </b-row>
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
    title: window.config.appName,
    date: new Date(),
    selected: null,
    options: [
      { value: null, text: '梱包仕様を選択してください' },
      { value: 1, text: '木箱梱包' },
      { value: 2, text: 'C/S(ケース／木箱)' },
      { value: 3, text: 'クレート梱包' },
      { value: 4, text: 'スキッド梱包' },
      { value: 5, text: 'パレット梱包' },
      { value: 6, text: '強化ダンボール' },
      { value: 7, text: 'スチール梱包' },
      { value: 8, text: 'スチールスキッド梱包' },
      { value: 9, text: 'ハイブリッド梱包' }
    ]
  }),

  computed: mapGetters({
    authenticated: 'auth/check'
  })
}
</script>

<style lang="scss" scoped>
  ::v-deep {
    .c {
      &-card {
        padding: 10px 18px;
        border-top: 4px solid #116ED6;
        box-shadow: 3px 3px 10px #707070;
        .title {
          font-family: 'Hiragino Mincho ProN', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
          font-size: 24px;
          font-weight: 600;
          &.btn {
            font-size: 20px;
            min-width: 218px;
          }
        }
        .item-text {
          font-family: Arial, Helvetica, sans-serif;
          font-size: 20px;
          font-weight: bold;
          color: #585858;
        }
        .chips {
          border-radius: 8px;
          background-color: #DDDDE5;
          font-family: Arial, Helvetica, sans-serif;
          font-size: 16px;
          font-weight: bold;
          color: #9294A3;
          min-width: 84px;
          text-align: center;
        }
        div.chips:not(:last-child) {
          margin-right: 16px;
        }
      }
      &-mx-5px {
        margin-left: 5px;
        margin-right: 5px;
      }
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
          background-color: #EBEBEB;
          border: 1px solid white;
          height: 60px;
          &.supplier {
            width: 67.3%;
          }
          &.w-arr {
            background-image: url(/assets/img/blue-arr.png);
            background-repeat: no-repeat;
            text-indent: 25px;
            background-position: 15px 50%;
          }
          &.custom-select {
            background: #EBEBEB url(/assets/img/blue-arr.png) no-repeat 15px 50%;
            padding: 6px 12px;
            text-indent: 25px;
            option {
              white-space: nowrap;
              text-overflow: ellipsis;
            }
          }
        }
        &-checkbox {
          font-family: 'Hiragino Kaku Gothic Pro', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
          font-size: 16px;
          font-weight: 300;
          color: #6E6E6E;
          .custom-control-label:before {
            background-color: #EBEBEB;
            border-radius: 6px;
          }
          .custom-control-input:checked ~ .custom-control-label::before {
            background-color: #007bff;
          }
        }
        &-btn {
          font-family: 'Hiragino Kaku Gothic Pro', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
          font-size: 26px;
          font-weight: 600;
          max-height: 60px;
          max-width: 80px;
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
      &-services {
        &-box {
          font-family: 'Hiragino Mincho ProN', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
          margin-top: 220px;
          margin-left: 45px;
          margin-right: 45px;
          color: #000;
        }
        &-title {
          font-size: 34px;
          font-weight: 600;
          margin-bottom: 36px;
          text-align: center;
        }
        &-sub-title {
          font-size: 22px;
          font-weight: 600;
          margin-bottom: 15px;
        }
        &-sub-text-content {
          font-size: 18px;
          font-weight: 600;
        }
        &-img {
          min-height: 150px;
          img {
            object-fit: contain;
          }
        }
      }
      &-products {
        &-box {
          font-family: 'Hiragino Mincho ProN', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
          margin-top: 115px;
          margin-left: 36px;
          margin-right: 36px;
          margin-bottom: 42px;
        }
        &-title {
          font-size: 34px;
          font-weight: 600;
          color: #333;
          margin-bottom: 55px;
        }
      }
    }
    .rm {
      &-border {
        &-bot {
          border-bottom: none;
        }
      }
      &-mx-calendar-icon {
        .mx-icon-calendar {
          display: none;
        }
      }
    }
  }
</style>
