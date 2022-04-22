<template>
  <div>
    <section class="head">
      <Menu />
      <business-banner></business-banner>
    </section>

    <section class="mainContent">
      <section class="section1 relative">
        <h1 class=" absolute top-0 right-0">希瑪家庭醫學中心 <span class=" block">MEDICINE CENTRE/</span></h1>
        <div class="content md:flex md:justify-between md:items-end">
          <div class="img"><img src="../../../assets/images/business/cmerfamily/section1.jpg" alt=""></div>
          <div class="small_card">
            <div class="logoimg"><img src="@/assets/images/business/cmerfamily/logo.svg" alt=""></div>
            <p>位於沙田之希瑪家庭醫學中心，由家庭醫學專科醫生石俊超醫生主理，對診治多種疾病方面具豐富經驗。家庭醫生專注於您和家人的健康，用心提供全面的醫療保健服務。醫生透過建立健康管理檔案，深入了解您的家族病史及家庭健康狀況，以專業知識及誠懇態度，構建長期、互信的醫患關係，關顧您人生不同階段的健康需要。 </p>
          </div>
        </div>
      </section>
      <section class="section2 relative md:flex md:items-center  md:justify-between">
        <div class="des_card">
          <p class=" text-justify">家庭醫生服務涵蓋疾病診斷和治療、健康綜合管理、制訂慢性疾病的持續和長期護理計劃，以至預防保健服務，例如健康檢查套餐、旅遊醫學和疫苗接種計劃。如有需要，醫生會根據病情所需，為您安排轉介相應專科，由來自不同領域的專科醫生進行跟進治療。</p>
        </div>

        <div class="img_social md:absolute ">
          <div class="img_slider  w-full"><img class="w-full" src="../../../assets/images/business/cmerfamily/section2.jpg" alt=""></div>
          <div class="social_box"></div>
        </div>
      </section>
      <div class="finally_des text-center "> 希瑪家庭醫學中心已列入2019 冠狀病毒病疫苗接種計劃的私家醫生/診所名單。</div>

    </section>

    <section class="foot">
      <Footer />
    </section>

  </div>
</template>

<script>
import "../../../assets/css/business/family/common.css"
import "../../../assets/css/business/family/mb.css"
import "../../../assets/css/business/family/pc.css"

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