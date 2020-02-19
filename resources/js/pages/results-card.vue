<template>
  <div>
    <div :class="detailToggle ? 'c-card blue' : 'c-card'">
      <b-row no-gutters="">
        <b-col cols="12" md="2" class="align-self-center">
          <h2 class="departure">
            出発地
          </h2>
          <div class="departure-date">
            2020/02/22
          </div>
        </b-col>
        <b-col cols="12" md="4" class="align-self-center">
          <h4 class="duration">
            3.5日間
          </h4>
          <div class="line-separator">
            <div class="h-line" />
            <div class="h-line-point" />
          </div>
          <div class="duration-supplier">
            5社経由
          </div>
        </b-col>
        <b-col cols="12" md="2" class="align-self-center">
          <h2 class="destination">
            横浜港
          </h2>
          <div class="destination-date">
            2020/02/25
          </div>
        </b-col>
        <b-col cols="12" md="4" class="align-self-center text-md-right">
          <h2 class="total-cost">
            ¥1,281,800
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
        v-for="(detail, index) in details"
        :key="index"
        class="detail-container"
      >
        <b-row no-gutters>
          <b-col cols="12" md="8">
            <div class="d-flex">
              <h2 class="supplier mb-0 mr-4">
                {{ detail.data1 }}
              </h2>
              <div class="chips">
                {{ detail.data2 }}
              </div>
            </div>
          </b-col>
          <b-col cols="12" md="4">
            <h4 class="text-md-right total-cost">
              {{ detail.data3 }}
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
                <span class="departure-date mr-3">{{ detail.data4 }}</span>
                <span class="departure">{{ detail.data5 }}</span>
              </div>
              <div>
                <span class="arrival-date mr-3">{{ detail.data6 }}</span>
                <span class="arrival">{{ detail.data7 }}</span>
              </div>
            </div>
            <div class="further-details">
              <h4 class="title">
                詳細
              </h4>
              <p class="content">
                {{ detail.data8 }}
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
      detailToggle: false,
      details: [
        {
          data1: '株式会社ABC運送',
          data2: 'トラック',
          data3: '¥400,000',
          data4: '2020/02/22',
          data5: '茨城県つくば市中山203-1',
          data6: '2020/02/22',
          data7: '横浜梱包有限会社',
          data8: '引取り料50,000円 \n輸送費350,000円／半日利用'
        },
        {
          data1: '横浜梱包有限会社',
          data2: '梱包',
          data3: '¥285,600',
          data4: '2020/02/22',
          data5: '横浜梱包有限会社',
          data6: '2020/02/23',
          data7: '横浜梱包有限会社',
          data8: '梱包費285,600円(M3単価10,000円)'
        },
        {
          data1: '横浜ロジスティクス株式会社',
          data2: '倉庫',
          data3: '¥571,200',
          data4: '2020/02/23',
          data5: '横浜ロジスティクス株式会社',
          data6: '2020/02/25',
          data7: '横浜ロジスティクス株式会社',
          data8: '保管料金：571,200円(M3単価5,000円)※フリータイムを除く4日間料金 \n保管日数：2週間(うちフリータイム10日間適応)'
        },
        {
          data1: '横浜ロジスティクス株式会社',
          data2: '通関',
          data3: '¥5,000',
          data4: '2020/02/22',
          data5: '横浜ロジスティクス株式会社',
          data6: '2020/02/25',
          data7: '横浜ロジスティクス株式会社',
          data8: '5,000円／一葉あたり'
        },
        {
          data1: '横浜ロジスティクス株式会社',
          data2: 'ドレージ',
          data3: '¥20,000',
          data4: '2020/02/25',
          data5: '横浜ロジスティクス株式会社',
          data6: '2020/02/25',
          data7: '横浜ロジスティクス株式会社',
          data8: 'なし'
        }
      ]
    }
  }
}
</script>

<style>

</style>
