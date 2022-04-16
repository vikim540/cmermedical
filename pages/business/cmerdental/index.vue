<template>
  <div>
    <section class="head">
      <Menu />
      <business-banner></business-banner>
    </section>

    <section class="mainContent">
      <div class="cmerdental_box1 md:flex md:justify-between md:items-center">
        <div class="title">
          <h2> 希瑪牙科 <span>CMER DENTAL/</span> </h2>
        </div>
        <div class="img_box">
          <div><img src="../../../assets/images/business/cmerdental/se1.jpg" alt=""></div>
          <div><img src="../../../assets/images/business/cmerdental/se2.jpg" alt=""></div>
          <div><img src="../../../assets/images/business/cmerdental/se3.jpg" alt=""></div>
        </div>

        <div class="small_card">
          <div class="logoimg"><img src="@/assets/images/business/cmerdental/logo.svg" alt=""></div>
          <p>中心致力為客戶提供專業貼心的牙齒檢查、牙科療程及美齒服務，全面服務範圍包括： </p>
        </div>

      </div>

      <ul class="service flex justify-between">
        <li>
          <div class=" text-center"><img src="../../../assets/images/business/cmerdental/seicon1.svg" alt=""></div>
          <h3 class=" text-center">基本牙科服務</h3>
          <p class=" text-center">牙齒、牙齦檢查及評估<br>
            洗牙<br>
            補牙<br>
            拔牙<br>
            提供口腔保健資訊</p>
        </li>

        <li>
          <div class=" text-center"><img src="../../../assets/images/business/cmerdental/seicon2.svg" alt=""></div>
          <h3 class=" text-center">修復及美容牙科</h3>
          <p class=" text-center">矯正牙齒<br>
            牙套及牙橋<br>
            牙托<br>
            牙齒美白<br>
            瓷牙貼片<br>
            全口修復</p>
        </li>

        <li>
          <div class=" text-center"><img src="../../../assets/images/business/cmerdental/seicon3.svg" alt=""></div>
          <h3 class=" text-center">高階牙科服務</h3>
          <p class=" text-center">電腦輔助即日口腔修復<br>
            智慧齒拔除<br>
            植牙<br>
            根管治療（杜牙根）<br>
            CBCT錐狀射束電腦斷層掃描<br>
            牙周病治療</p>
        </li>
      </ul>

      <div class=" img_show md:flex md:items-end">
        <div class="md:flex-1"><img class="w-full" src="@/assets/images/business/cmerdental/slider_bg.jpg" alt=""></div>
        <div class="relative md:flex-1">
          <div class="img_slider md:absolute"><img class=" w-full " src="@/assets/images/business/cmerdental/slider1.jpg" alt=""></div>
          <div class="social_box"></div>
        </div>
      </div>

      

     

      <div class="more_box">
        <div class="md:flex md:justify-between more_content">
          <div class="des">
            <p>全港七間希瑪牙科中心設有國際認可的牙齒健康檢測機器及牙科專業儀器，務求為患者提供最準確的診斷及優質的牙科服務。
            </p>
            <p>
              此外，牙科中心秉持「整體分析」的原則，根據客戶的實際口腔健康狀況制定嚴格且針對性的治療。我們亦注重口腔衛生教育，希望透過推廣牙齒健康的重要性，提高大眾對口腔護理的關注。
            </p>
            <a href="" class="more_link">了解更多 <span class="fa_right"><i class="fa fa-angle-right "></i></span> </a>
          </div>
          <div class="img">
            <img src="../../../assets/images/business/cmerdental/moreimg.jpg" alt="">
          </div>
        </div>
      </div>
    </section>

    <section class="foot">
      <Footer />
    </section>

  </div>
</template>

<script>
import "../../../assets/css/business/cmerdental/common.css"
import "../../../assets/css/business/cmerdental/mb.css"
import "../../../assets/css/business/cmerdental/pc.css"

import InnerSlider from "@/components/commom/slider/InnerSlider.vue"
import Menu from "@/components/commom/head/Menu.vue"
import Footer from "@/components/commom/foot/Footer.vue"
import BusinessBanner from "@/components/commom/banner/BusinessBanner.vue"
export default {
  components: { Menu, Footer, BusinessBanner, InnerSlider },
  data() {
    return {

    };
  },
  created() { },
  methods: {}
};
</script>

<style scoped>
</style>