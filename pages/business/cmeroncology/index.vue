<template>
  <div>
    <section class="head">
      <Menu />
      <business-banner></business-banner>
    </section>

    <section class="mainContent">
      <section class="section1 relative">
        <div class="title absolute top-0 right-0">
          <h2>
            希瑪中西腫瘤專科
            <span class="block">ONCOLOGY/</span>
          </h2>
        </div>

        <div class="small_card md:relative">
          <div class="logoimg">
            <img src="@/assets/images/business/cmeroncology/logo.svg" alt />
          </div>
          <p>座落中環之希瑪（環球）醫療中心，由香港臨床腫瘤科醫生廖少輝醫生主理，醫療團隊在中西醫學領域擁有多年的經驗，為癌症患者提供優質中西結合的腫瘤科專科醫療服務。</p>
          <p>希瑪中西腫瘤專科為病人診斷、設計及執行整個療程及療後的護理。全面的服務範圍包括：</p>
        </div>

        <div class="img md:absolute top-0 right-0">
          <img class="w-full" src="../../../assets/images/business/cmeroncology/section1.jpg" alt />
        </div>
      </section>

      <section class="section2 md:flex md:justify-center">
        <div class="item md:flex-1">
          <div class="flex justify-center">
            <img class src="../../../assets/images/business/ameraesthetics/section2_1.svg" alt />
          </div>
          <h3 class="text-center">美學塑造</h3>
          <p class="text-center">
            明亮雙眸
            <br />緊緻輪廓
            <br />側輪廓塑造
            <br />耳廓塑造
            <br />美乳塑造
            <br />消脂纖體
          </p>
        </div>

        <div class="item md:flex-1">
          <div class="flex justify-center">
            <img src="../../../assets/images/business/ameraesthetics/section2_2.svg" alt />
          </div>
          <h3 class="text-center">醫學亮肌</h3>
          <p class="text-center">
            緊膚緹拉
            <br />營養注入
            <br />光學美膚
          </p>
        </div>

        <div class="item md:flex-1">
          <div class="flex justify-center">
            <img src="../../../assets/images/business/ameraesthetics/section2_3.svg" alt />
          </div>
          <h3 class="text-center">嫩肌護理</h3>
          <p class="text-center">
            女神機RF緊膚
            <br />女神機RF緊緻眼部
            <br />暗瘡抗炎降紅護理
            <br />積雪草舒敏護理
            <br />膠原蛋白再生護理
            <br />透明質酸保濕護理
            <br />B5特效保濕
            <br />Aqua Pure 淨膚滋養護理
          </p>
        </div>
      </section>

      <section class="section3 md:flex md:items-center md:justify-end md:relative">
        <div class="left md:absolute md:bottom-0 left-0">
          <div class="img_slider w-full">
            <img class="w-full" src="../../../assets/images/business/cmeroncology/section3.jpg" alt />
          </div>
        </div>
        <div class="right">
          <p class="text-justify">預防勝於治療，醫療中心同時提供HPV疫苗注射。9 合 1 HPV疫苗可預防9 種病毒類型所引致之常見高危疾病及癌症，減低感染及患上子宮頸癌、陰道癌及肛門癌的機會。</p>
          <a href class="more_link">
            了解更多
            <span class="fa_right">
              <i class="fa fa-angle-right"></i>
            </span>
          </a>
        </div>
      </section>

      <section class="section4 md:flex md:items-end">
        <div class="md:flex-1">
          <img class="w-full" src="../../../assets/images/business/cmeroncology/section4_bg.jpg" alt />
        </div>
        <div class="relative md:flex-1">
          <div class="img_slider md:absolute">
            <img class="w-full" src="../../../assets/images/business/cmeroncology/section4_slider_img1.jpg" alt />
          </div>
          <div class="social_box"></div>
        </div>
      </section>
    </section>

    <section class="foot">
      <Footer />
    </section>
  </div>
</template>

<script>
import "@/assets/css/business/cmeroncology/common.css"
import "@/assets/css/business/cmeroncology/mb.css"
import "@/assets/css/business/cmeroncology/pc.css"

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