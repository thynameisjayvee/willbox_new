<template>
  <div>
    <div :class="detailToggle ? 'c-card blue' : 'c-card'">
      <b-row no-gutters="">
        <b-col cols="12" md="2" class="align-self-center">
          <h2 class="departure">
            出発地
          </h2>
          <div class="departure-date">
            2020/01/25
          </div>
        </b-col>
        <b-col cols="12" md="4" class="align-self-center">
          <h4 class="duration">
            8日間
          </h4>
          <div class="line-separator">
            <div class="h-line" />
            <div class="h-line-point" />
          </div>
          <div class="duration-supplier">
            3社経由
          </div>
        </b-col>
        <b-col cols="12" md="2" class="align-self-center">
          <h2 class="destination">
            出発地
          </h2>
          <div class="destination-date">
            2020/01/25
          </div>
        </b-col>
        <b-col cols="12" md="4" class="align-self-center text-md-right">
          <h2 class="total-cost">
            ¥1,250,000
          </h2>
          <div v-if="!detailToggle">
            <b-button variant="primary" squared class="total-cost-btn" @click="detailToggle = !detailToggle">
              プラン詳細へ
            </b-button>
          </div>
          <div v-else>
            <b-button variant="primary" squared class="total-cost-btn">
              PDFダウンロード
            </b-button>
            <b-button @click="detailToggle = !detailToggle">
              <b-icon-chevron-compact-up />
            </b-button>
          </div>
        </b-col>
      </b-row>
    </div>
    <div v-if="detailToggle" class="results-detail">
      <div
        v-for="index in 3"
        :key="index"
        class="detail-container"
      >
        <b-row no-gutters>
          <b-col cols="12" md="8">
            <div class="d-flex">
              <h2 class="supplier mb-0 mr-4">
                株式会社○○
              </h2>
              <div class="chips">
                梱包
              </div>
            </div>
          </b-col>
          <b-col cols="12" md="4">
            <h4 class="text-md-right total-cost">
              ¥1,250,000
            </h4>
          </b-col>
        </b-row>
        <b-row no-gutters>
          <b-col cols="12" md="8">
            <div class="travel-container">
              <div class="left-border-circle">
                <b-icon-circle class="up" />
                <b-icon-circle class="down" />
              </div>
              <div>
                <span class="departure-date mr-3">2020/01/25</span>
                <span class="departure">出発地</span>
              </div>
              <div>
                <span class="arrival-date mr-3">2020/01/27</span>
                <span class="arrival">株式会社○○運送 倉庫</span>
              </div>
            </div>
            <div class="further-details">
              <h4 class="title">
                詳細
              </h4>
              <p class="content">
                ○○○○○○○○○○○○○○○○○○○○
                ○○○○○○○○○○○○。
                ○○○○○○○○○○○○○○○○○○○○
                ○○○○○○○○○○○○○○○○○○。
              </p>
            </div>
          </b-col>
          <b-col cols="12" md="4">
            <div class="w-50 ml-md-auto">
              <star-rating
                :star-size="16"
                rating="4"
                :padding="8"
                read-only
                :show-rating="false"
                border-color="#ffd055"
              />
            </div>
          </b-col>
        </b-row>
        <hr>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      detailToggle: false
    }
  }
}
</script>

<style>

</style>
