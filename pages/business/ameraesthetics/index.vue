<template>
  <div>
    <section class="head">
      <Menu />
      <business-banner></business-banner>
    </section>

    <section class="mainContent">
      <section class="section1 relative">
        <div class="title absolute top-0 right-0">
          <h2> 愛瑪醫美 <span class=" block">MEDICAL AESTHETICS/</span> </h2>
        </div>

        <div class="content md:flex md:justify-between">
          <div class="img_box md:flex md:items-center md:justify-center">
            <img class="img2" src="../../../assets/images/business/ameraesthetics/section1_2.jpg" alt="">
            <img class="img1" src="../../../assets/images/business/ameraesthetics/section1_1.jpg" alt="">

          </div>
          <div class="small_card">
            <div class="logoimg"><img src="@/assets/images/business/ameraesthetics/logo.svg" alt=""></div>
            <p>我們以「簡單‧美」為宗旨，提供全方位身體和面部治療方案，讓客戶展現個人特色自然美。 </p>
            <p>愛瑪醫美全面化的服務項目包括:</p>
          </div>

          <div class="bg_text absolute bottom-0 right-0">
            <span class=" block">/SIMPLE </span>
            <span>IS BEAUTIFUL</span>
          </div>
        </div>
      </section>

      <section class=" section2 md:flex   md:justify-center">
        <div class="item md:flex-1">
          <div class="flex justify-center "><img class="" src="../../../assets/images/business/ameraesthetics/section2_1.svg" alt=""></div>
          <h3 class="text-center">美學塑造</h3>
          <p class="text-center">
            明亮雙眸<br>
            緊緻輪廓<br>
            側輪廓塑造<br>
            耳廓塑造<br>
            美乳塑造<br>
            消脂纖體</p>
        </div>

        <div class="item md:flex-1">
          <div class="flex justify-center "><img src="../../../assets/images/business/ameraesthetics/section2_2.svg" alt=""></div>
          <h3 class="text-center">醫學亮肌</h3>
          <p class="text-center">
            緊膚緹拉<br>
            營養注入<br>
            光學美膚</p>
        </div>

        <div class="item md:flex-1">
          <div class="flex justify-center "><img src="../../../assets/images/business/ameraesthetics/section2_3.svg" alt=""></div>
          <h3 class="text-center">嫩肌護理</h3>
          <p class="text-center">
            女神機RF緊膚<br>
            女神機RF緊緻眼部<br>
            暗瘡抗炎降紅護理<br>
            積雪草舒敏護理<br>
            膠原蛋白再生護理<br>
            透明質酸保濕護理<br>
            B5特效保濕<br>
            Aqua Pure 淨膚滋養護理</p>
        </div>
      </section>

      
      <section class="section3 md:flex md:items-center md:justify-end md:relative ">
        <div class="left md:absolute md:bottom-0 left-0">
          <div class="img_slider w-full"><img class="w-full" src="../../../assets/images/business/ameraesthetics/section3.jpg" alt=""></div>
          <div class="social_box"></div>
        </div>
        <div class="right ">
          <p class=" text-justify">醫美中心配備嶄新醫學美容儀器，並已獲得美國FDA或歐盟CE相關認證，配合醫護團隊的審美觸覺，為客戶制訂專屬的自然美學方案，確保療程安全、有效、可靠。</p>
          <a href="" class="more_link">了解更多 <span class="fa_right"><i class="fa fa-angle-right "></i></span> </a>
        </div>
      </section>
    </section>

    <section class="foot">
      <Footer />
    </section>

  </div>
</template>

<script>
import "@/assets/css/business/ameraesthetics/common.css"
import "@/assets/css/business/ameraesthetics/mb.css"
import "@/assets/css/business/ameraesthetics/pc.css"

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