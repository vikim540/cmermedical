<template>
  <div class="section_anti">
    <section class="head">
      <Menu />

      <div class="banner relative">
        <span class="absolute">抗疫專區</span>
      </div>

    </section>

    <section class="mainContent">
      <h1 class=" text-center font-black">\全民齊心抗疫 希瑪<span>「疫」</span>境同行/</h1>
      <p class=" text-justify">守護市民健康、促進社會福祉代表著希瑪醫療履行社會責任的核心理念。香港受新冠肺炎第五波Omicron疫情嚴重衝擊下，市民對病毒檢測的需求非常殷切。為保障基層大眾獲得優質且供應充裕的快速檢測包，希瑪醫療於2022年2月18日獲深圳市亞輝龍生物科技股份有限公司授權成為YHLO新冠金標抗原檢測試劑盒 (GLINE-2019-NCOV AG) 在香港地區的獨家總經銷商。</p>
      <div class="text_img md:flex ">
        <p class=" text-justify">希瑪醫療更聯同亞輝龍合共捐出120萬套快速檢測包，透過與超過70個慈善團體和非牟利機構夥伴合作，免費派發給基層市民。重點受助對象主要是高風險或需要定期病毒檢測行業的人士，包括安老及護理院舍、清潔、保安行業員工、的士和小巴司機、長期病患者及劏房家庭。透過與港人同心攜手全面抗疫，進一步體現希瑪醫療積極履行企業社會責任的努力。</p>
        <img src="../../assets/images/anti/p2.jpg" alt="">
      </div>
      <p class=" text-justify">快速檢測包捐贈行動獲得受助機構積極的正面回饋，形容這次捐贈對他們來説是一個很大的及時雨，免卻弱勢社群奔波購買檢測包的煩惱，同時紓緩他們的經濟負擔。</p>
      <img class="tail_img w-full" src="../../assets/images/anti/p3.jpg" alt="">
      <p class="tail_text">港人團結抗疫，發揮獅子山精神，沒有香港人跨不過的難關！</p>
    </section>
    <section class="foot">
      <Footer />
    </section>

  </div>
</template>

<script>

import "../../assets/css/anti/common.css"
import "../../assets/css/anti/mb.css"
import "../../assets/css/anti/pc.css"


import Menu from "@/components/commom/head/Menu.vue"
import Footer from "@/components/commom/foot/Footer.vue"
export default {
  components: { Menu, Footer, },
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