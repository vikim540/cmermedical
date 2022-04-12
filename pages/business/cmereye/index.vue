<template>
  <div>
    <section class="head">
      <Menu />
      <business-banner></business-banner>
    </section>

    <section class="mainContent">
      <div class="eye_list">
        <div class="eye_item flex" v-for="(eyeItem,index) in eyeList" :key="index">
          <div class="left">
            <div class="title flex items-end ">
              <h2>{{eyeItem.title}}<span>{{eyeItem.titleEn}}</span></h2>
              <span class="index">0{{index+1}}</span>
            </div>

            <div class="info">
              <div class="logoimg"><img :src="eyeItem.logo" alt=""></div>
              <p>{{eyeItem.description}}</p>
              <a :href="eyeItem.moreLink" class="more_link">了解更多 <span class="fa_right"><i class="fa fa-angle-right "></i></span> </a>
            </div>
          </div>

          <div class="right">
            <div class="slider_img"><img src="../../../assets/images/business/cmereye/eyecenter1.jpg" alt=""></div>
            <div class="social"></div>
          </div>
        </div>
      </div>
      <div class="info_from">資料來源：
        <br>＃ 香港人口推算 2020-2069，政府統計處，2020年9月出版。
        <br> ＊ 香港中文大學醫學院新聞稿，2021年8月30日。
      </div>
    </section>

    <section class="foot">
      <Footer />
    </section>

  </div>
</template>

<script>
import Menu from "@/components/commom/head/Menu.vue"
import BusinessBanner from "@/components/commom/banner/BusinessBanner.vue"
import Footer from "@/components/commom/foot/Footer.vue"
export default {
  components: { Menu, Footer, BusinessBanner },
  data() {
    return {
      eyeList: [
        {
          title: '希瑪林順潮眼科中心',
          titleEn: 'EYE CENTER/',
          logo: require('../../../assets/images/business/cmereye/eyecenterlogo.svg'),
          description: '希瑪醫療具備多名豐富經驗的眼科專科醫生，各有不同專長，加上註冊視光師及醫療護理人員組成團隊。眼科中心嚴格遵守香港及國際醫療技術操作規範，設有多間符合國際標準的無菌手術室，配備先進尖端的眼科醫療儀器，為客戶提供安全、準確、可靠的眼科檢查及醫療服務。',
          moreLink: '',
          SliderImgSrcList: [
            require('../../../assets/images/business/cmereye/eyecenter1.jpg'),
            require('../../../assets/images/business/cmereye/eyecenter1.jpg'),
            require('../../../assets/images/business/cmereye/eyecenter1.jpg'),
            require('../../../assets/images/business/cmereye/eyecenter1.jpg'),
            require('../../../assets/images/business/cmereye/eyecenter1.jpg'),
          ],
          socialLinkList: [{ la: '' }, { fb: '' }, { wa: '' }, { wx: '' }, { em: '' }]
        },
        {
          title: '微笑激光矯視中心',
          titleEn: 'SMILE REFRACTIVE CENTER/',
          logo: require('../../../assets/images/business/cmereye/eyesmilelogo.svg'),
          description: '首批在香港率先引入激光矯視技術，希瑪微笑矯視中心以美國FDA激光矯視手術的標準要求為準則，根據客戶的不同情況度身訂造嚴格且有針對性的矯視方案。中心的服務範圍包括SMILE微笑激光矯視、LASIK激光矯視、植入式隱形眼鏡(ICL)、人工晶體置換術 (IOL) 及配鏡服務等等，幫助患有近視、遠視、散光、老花及白內障的客戶改善視力。',
          moreLink: '',
          SliderImgSrcList: [
            require('../../../assets/images/business/cmereye/eyesmile1.jpg'),
            require('../../../assets/images/business/cmereye/eyesmile1.jpg'),
            require('../../../assets/images/business/cmereye/eyesmile1.jpg'),
            require('../../../assets/images/business/cmereye/eyesmile1.jpg'),
            require('../../../assets/images/business/cmereye/eyesmile1.jpg'),
          ],
          socialLinkList: [{ la: '' }, { fb: '' }, { wa: '' }, { wx: '' }, { em: '' }]
        },
        {
          title: '視光中心',
          titleEn: 'VISION CENTER/',
          logo: require('../../../assets/images/business/cmereye/eyevisionlogo.svg'),
          description: '希瑪眼科視光中心致力為客戶提供全面眼科視光檢查及眼睛護理，根據不同年齡層的眼睛狀況及個人實際所需，制定專屬的眼睛檢查及護眼建議，並提供一站式安全、準確及可靠的改善視力方案。針對學童近視率偏高的問題，視光中心會為兒童提供詳細眼睛檢查服務及針對性的兒童近視控制方案，助兒童把握控制近視的黃金治療期。',
          moreLink: '',
          SliderImgSrcList: [
            require('../../../assets/images/business/cmereye/eyevision1.jpg'),
            require('../../../assets/images/business/cmereye/eyevision1.jpg'),
            require('../../../assets/images/business/cmereye/eyevision1.jpg'),
            require('../../../assets/images/business/cmereye/eyevision1.jpg'),
            require('../../../assets/images/business/cmereye/eyecenter1.jpg'),
          ],
          socialLinkList: [{ la: '' }, { fb: '' }, { wa: '' }, { wx: '' }, { em: '' }]
        }
      ]
    };
  },
  created() { },
  methods: {}
};
</script>

<style scoped>
.eye_item {
  width: 80vw;
  margin: 15vw auto;
  background: #f3f3f3;
  padding: 4vw 0 3vw 4vw;
}
.eye_item .left {
  margin-right: 4vw;
  position: relative;
}
.eye_item .left .title {
  color: #80c5de;
  white-space: pre-wrap;
  position: absolute;
  top: -12.2vw;
  left: -6.5vw;
}
.eye_item .left .title h2 {
  font-size: 1.5vw;
  line-height: 0.5vw;
}
.eye_item .left .title h2 > span {
  display: block;
  font-size: 3vw;
  line-height: 4vw;
}
.eye_item .left .title .index {
  font-size: 10vw;
  line-height: 10vw;
  margin-left: 5vw;
}
.eye_item .left .info {
  background: #fff;
  padding: 3vw;
  width: 35vw;
}
.eye_item .left .info p {
  text-indent: 2.2vw;
  text-align: justify;
  margin-top: 1vw;
}
.eye_item .left .info .logoimg {
  padding-bottom: 1.5vw;
  position: relative;
}
.eye_item .left .info .logoimg img {
  width: 10vw;
}
.eye_item .left .info .logoimg::before {
  position: absolute;
  content: " ";
  width: 7vw;
  border-bottom: 2px solid #f09038;
  bottom: 0;
}
.eye_item .left .info .logoimg::after {
  position: absolute;
  content: " ";
  width: 1vw;
  height: 1vw;
  border: 2px solid #80c5de;
  border-left: none;
  border-bottom: none;
  top: 0;
  right: 0;
}

.eye_item .right {
}
.eye_item .right .slider_img {
  width: 39vw;
  margin-top: -8vw;
}

.mainContent .eye_list .eye_item:nth-child(2) {
  padding: 4vw 4vw 3vw 0;
}

.mainContent .eye_list .eye_item:nth-child(2) .left {
  order: 2;
  margin-right: 0;
  margin-left: 4vw;
}
.mainContent .eye_list .eye_item:nth-child(2) .left .title {
  left: -12vw;
  white-space: nowrap;
}
.mainContent .eye_list .eye_item:nth-child(2) .left .title h2 {
  order: 2;
}

.mainContent .eye_list .eye_item:nth-child(2) .left .title .index {
  margin-left: 0;
  margin-right: 5vw;
}
.mainContent .eye_list .eye_item:nth-child(2) .right {
  order: 1;
  margin-left: -2vw;
}

.footer {
  margin-top: 2vw;
}
.info_from {
  margin-left: 7vw;
}
</style>