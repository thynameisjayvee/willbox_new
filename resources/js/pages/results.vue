<template>
  <div class="container-fluid px-0">
    <form action="" class="bg-white">
      <div class="extend-strip">
        <div class="container-fluid px-0">
          <div class="form-header">
            <b-row no-gutters>
              <b-col cols="12" md="2" class="pr-3 py-1">
                <label class="mb-0">搬入港</label>
                <b-form-input
                  class="w-arr--white"
                  type="text"
                  value="横浜港"
                  placeholder="test"
                />
              </b-col>
              <b-col cols="12" md="3" class="px-3 py-1 border-left">
                <label class="mb-0">CYカット日</label>
                <b-form-input
                  class="w-arr--white"
                  type="text"
                  value="2020/02/28"
                  placeholder="test"
                />
              </b-col>
              <b-col cols="12" md="4" class="px-3 py-1 border-left">
                <label class="mb-0">出発地</label>
                <b-form-input
                  class="w-arr--white"
                  type="text"
                  value="茨城県つくば市中山203-1"
                  placeholder="test"
                />
              </b-col>
              <b-col cols="12" md="3" class="px-3 py-1 border-left">
                <label class="mb-0">梱包仕様</label>
                <b-form-input
                  class="w-arr--white"
                  type="text"
                  value="C/S(ケース／木箱)"
                  placeholder="test"
                />
              </b-col>
            </b-row>
          </div>
        </div>
      </div>
      <div class="form-body">
        <div class="white-strip" />
        <b-tabs content-class="mt-3" nav-class="c-tabs border-bottom-0" active-nav-item-class="c-tabs--active">
          <b-tab active>
            <template #title>
              <div class="c-tabs--title">
                <img src="assets/img/car.png" alt="car-icon">
                <span style="vertical-align: middle;">トラック</span>
              </div>
            </template>
            <b-row class="mt-4" no-gutters>
              <b-col cols="12">
                <b-form-input
                  class="supplier"
                  type="text"
                  placeholder="test"
                  value="株式会社ABC運送"
                />
              </b-col>
              <h2 class="product-info">
                製品情報
              </h2>
              <b-col cols="12">
                <b-row no-gutters>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      type="text"
                      value="3,400" placeholder="長さ(L) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      value="2,800" placeholder="幅(W) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      value="3,000" placeholder="高さ(H) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      value="5,000" placeholder="製品重量 kg"
                    />
                  </b-col>
                  <b-col cols="12" md="2" class="d-flex align-items-center justify-content-center">
                    <b-form-checkbox-group
                      v-model="selected"
                      class="c-checkbox"
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
              </b-col>
            </b-row>
          </b-tab>
          <b-tab>
            <template #title>
              <div class="c-tabs--title">
                <img src="assets/img/package.png" alt="package-icon">
                <span style="vertical-align: middle;">梱包</span>
              </div>
            </template>
            <b-row class="mt-4" no-gutters>
              <b-col cols="12">
                <b-form-input
                  class="supplier"
                  type="text"
                  placeholder="test"
                  value="株式会社ABC運送"
                />
              </b-col>
              <h2 class="product-info">
                製品情報
              </h2>
              <b-col cols="12">
                <b-row no-gutters>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      type="text"
                      value="3,400" placeholder="長さ(L) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      value="2,800" placeholder="幅(W) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      value="3,000" placeholder="高さ(H) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      value="5,000" placeholder="製品重量 kg"
                    />
                  </b-col>
                  <b-col cols="12" md="2" class="d-flex align-items-center justify-content-center">
                    <b-form-checkbox-group
                      v-model="selected"
                      class="c-checkbox"
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
              </b-col>
            </b-row>
          </b-tab>
          <b-tab>
            <template #title>
              <div class="c-tabs--title">
                <img src="assets/img/notes.png" alt="notes-icon">
                <span style="vertical-align: middle;">通関</span>
              </div>
            </template>
            <b-row class="mt-4" no-gutters>
              <b-col cols="12">
                <b-form-input
                  class="supplier"
                  type="text"
                  placeholder="test"
                  value="株式会社ABC運送"
                />
              </b-col>
              <h2 class="product-info">
                製品情報
              </h2>
              <b-col cols="12">
                <b-row no-gutters>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      type="text"
                      value="3,400" placeholder="長さ(L) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      value="2,800" placeholder="幅(W) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      value="3,000" placeholder="高さ(H) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      value="5,000" placeholder="製品重量 kg"
                    />
                  </b-col>
                  <b-col cols="12" md="2" class="d-flex align-items-center justify-content-center">
                    <b-form-checkbox-group
                      v-model="selected"
                      class="c-checkbox"
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
              </b-col>
            </b-row>
          </b-tab>
          <b-tab>
            <template #title>
              <div class="c-tabs--title">
                <img src="assets/img/warehouse.png" alt="warehouse-icon">
                <span style="vertical-align: middle;">倉庫保管</span>
              </div>
            </template>
            <b-row class="mt-4" no-gutters>
              <b-col cols="12">
                <b-form-input
                  class="supplier"
                  type="text"
                  placeholder="test"
                  value="株式会社ABC運送"
                />
              </b-col>
              <h2 class="product-info">
                製品情報
              </h2>
              <b-col cols="12">
                <b-row no-gutters>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      type="text"
                      value="3,400" placeholder="長さ(L) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      value="2,800" placeholder="幅(W) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      value="3,000" placeholder="高さ(H) mm"
                    />
                  </b-col>
                  <b-col cols="12" md="2">
                    <b-form-input
                      class="w-arr"
                      value="5,000" placeholder="製品重量 kg"
                    />
                  </b-col>
                  <b-col cols="12" md="2" class="d-flex align-items-center justify-content-center">
                    <b-form-checkbox-group
                      v-model="selected"
                      class="c-checkbox"
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
              </b-col>
            </b-row>
          </b-tab>
        </b-tabs>
      </div>
    </form>
    <div class="results-body">
      <b-row no-gutters>
        <b-col v-for="index in 6" :key="index" cols="12" class="mb-5">
          <v-result-card />
        </b-col>
      </b-row>
    </div>
  </div>
</template>

<script>
import ResultsCard from './results-card'

export default {
  components: {
    'v-result-card': ResultsCard
  },

  metaInfo () {
    return { title: this.$t('results') }
  },

  data: () => ({
    title: window.config.appName,
    detailToggle: false,
    selected: ['引取り']
  })
}
</script>

<style lang="scss" scoped>
  ::v-deep {
    .extend-strip {
      width: 100%;
      background-color: #0580FD;
      .container-fluid {
        width: 1170px;
        margin-left: auto;
        margin-right: auto;
        min-height: inherit;
      }
    }
    .form-header {
      max-width: 920px;
      margin-left: auto;
      margin-right: auto;
      font-family: 'Hiragino Kaku Gothic Pro', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      color: white;
      label {
        font-size:  18px;
        font-weight: 300;
      }
      input {
        background-color: #0580fd;
        border-color: #0580fd;
        font-size: 20px;
        font-weight: 300;
        color: white;
        max-height: 30px;
        white-space: nowrap;
        text-overflow: ellipsis;
        &::placeholder {
          color: white;
        }
        &.w-arr--white {
          background-image: url(/assets/img/white-arr.png);
          background-repeat: no-repeat;
          text-indent: 8px;
          background-position: 0 50%;
        }
      }
      .border-left {
        border-left: 1px solid #fff;
      }
    }
    .form-body {
      background-color: #fff;
      max-width: 920px;
      margin-left: auto;
      margin-right: auto;
      padding: 18px 0;
      font-family: 'Hiragino Kaku Gothic Pro', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      color: #7B7B7B;
      position: relative;
      .white-strip {
        background: white;
      }
      .c-tabs {
        .nav-link {
          padding: 4px 8px;
          height: 100%;
          border-bottom: 1px solid #C3C3C3;
        }
        li:not(:last-child) {
          margin-right: 70px;
        }
        &--title {
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
      .c-checkbox {
        font-family: 'Hiragino Kaku Gothic Pro', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 16px;
        font-weight: 300;
        color: #6E6E6E;
        box-shadow: none;
        &:focus {
          outline: none;
        }
        .custom-control-label:before {
          background-color: #EBEBEB;
          border-radius: 6px;
        }
        .custom-control-input:checked ~ .custom-control-label::before {
          background-color: #007bff;
        }
      }
      .c-search-btn {
        font-size: 26px;
        font-weight: 600;
        max-height: 60px;
        max-width: 80px;
      }
      input {
        font-family: 'Hiragino Kaku Gothic Pro', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 16px;
        font-weight: 300;
        color: #6E6E6E;
        background-color: #EBEBEB;
        border-color: #fff;
        min-height: 60px;
        text-indent: 20px;
        box-shadow: none;
        &.supplier {
          width: 71%;
        }
        &.w-arr {
          background-image: url(/assets/img/blue-arr.png);
          background-repeat: no-repeat;
          text-indent: 25px;
          background-position: 15px 50%;
        }
      }
      .product-info {
        font-size: 18px;
        font-weight: 600;
        margin: 12px 0px;
      }
    }
    .results-body {
      margin-top: 46px;
      max-width: 920px;
      margin-left: auto;
      margin-right: auto;
      font-family: 'Hiragino Kaku Gothic Pro', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      .c-card {
        background-color: #fff;
        border-top: 4px solid #0580FD;
        padding: 26px 105px;
        &.blue {
          background-color: #0580FD;
          transition: background-color 0.5s ease;
          color: #fff;
          .departure, .departure-date, .destination, .destination-date,
          .duration, .duration-supplier,
          .total-cost {
            color: white;
          }
          .line-separator {
            border-color: white;
          }
          .total-cost-btn {
            background-color: white;
            color: black;
            font-size: 18px;
          }
        }
        .departure, .destination {
          font-size: 22px;
          font-weight: 300;
          color: #000;
          &-date {
            font-family: Arial, Helvetica, sans-serif;
            font-size: 20px;
            color: #7B7B7B;
          }
        }
        .duration {
          font-family: Arial, Helvetica, sans-serif;
          font-size: 18px;
          color: #7B7B7B;
          text-align: center;
          margin-bottom: 0;
          &-supplier {
            font-size: 20px;
            font-weight: 300;
            color: #116ED6;
            text-align: center;
          }
        }
        .total-cost {
          font-family: Arial, Helvetica, sans-serif;
          font-size: 32px;
          font-weight: bold;
          color: #333;
          &-btn {
            min-height: 35px;
            min-width: 162px;
            font-size: 20px;
            font-weight: 600;
          }
        }
      }
    }
    .results-detail {
      padding-top: 40px;
      padding-bottom: 40px;
      max-width: 920px;
      background-color: white;
      margin-left: auto;
      margin-right: auto;
      font-family: 'Hiragino Kaku Gothic Pro', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      .detail-container {
        max-width: 700px;
        margin-right: auto;
        margin-left: auto;
        .supplier {
          font-size: 20px;
          font-weight: 300;
          color: #000;
        }
        .chips {
          border-radius: 8px;
          background-color: #DDDDE5;
          font-family: Arial, Helvetica, sans-serif;
          font-size: 14px;
          font-weight: bold;
          color: #9294A3;
          min-width: 84px;
          text-align: center;
        }
        .total-cost {
          font-family: Arial, Helvetica, sans-serif;
          font-size: 26px;
          font-weight: bold;
        }
        .travel-container {
          position: relative;
          min-height: 87px;
          display: flex;
          flex-direction: column;
          justify-content: space-between;
          padding-left: 32px;
          .left-border-circle {
            height: 75%;
            border-left: 2px solid #A8A8A8;
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            left: 8px;
            .up {
              position: absolute;
              top: -6px;
              left: -9px;
              background-color: white;
            }
            .down {
              position: absolute;
              bottom: -6px;
              left: -9px;
              background-color: white;
            }
          }
          .departure, .arrival {
            font-size: 20px;
            font-weight: 300;
            color: #000000;
            &-date {
              font-size: 20px;
              color: #000;
              font-family: Arial, Helvetica, sans-serif;
            }
          }
        }
        .further-details {
          padding-left: 32px;
          margin-top: 56px;
          .title {
            font-size: 20px;
            font-weight: 300;
          }
          .content {
            font-size: 20px;
            font-weight: 300;
            margin-bottom: 0px;
          }
        }
      }
    }
    .line-separator {
      border-color: #909090;
      .h-line {
        display: inline-block;
        border-top: 1px solid;
        width: calc(100% - 7px);
      }
      .h-line-point {
        display: inline-block;
        border-top: 1px solid;
        transform: rotate(45deg);
        height: 6px;
        width: 12px;
        margin-left: -7%;
      }
    }
  }
</style>
