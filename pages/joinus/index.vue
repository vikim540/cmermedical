<template>
  <div class="section_joinus">
    <section class="head">
      <Menu />
      <div class="banner relative">
        <div class="absolute title_box">
          <span class=" block text-white ">加入我們</span>
          Work With Us/
        </div>
        <div class="bluetitle_box text-white absolute">人才為本 共同成長</div>
      </div>

    </section>

    <section class="mainContent">
      <section class="section1 relative ">
        <p class=" text-center flex justify-center ">
          希瑪醫療能夠取得長足發展，<br>
          實有賴全體員工堅守專業精神及熱誠工作態度，同心協力，<br>
          為客人提供「度身訂造」的綜合醫療服務。
        </p>
      </section>
      <section class="section2">
        <h2 class="flex items-center justify-center font-black wow animate__animated animate__fadeInUp" data-wow-duration="1s" data-wow-delay="0s">員工<img src="@/assets/images/home/title1.svg" alt="">文化</h2>

        <ul class=" flex flex-col md:justify-end">
          <li class="md:ml-auto relative">
            <img src="../../assets/images/joinus/section2_1.jpg" alt="">
            <div class="text absolute">
              <h3>共同成長</h3>
              <p>希瑪醫療重視員工的發展及培訓，為新加入的醫生及護士提供指導，幫助他們掌握嶄新技術，熟悉公司的服務標準、政策及程序。</p>
            </div>
          </li>

          <li class=" relative">
            <img src="../../assets/images/joinus/section2_2.jpg" alt="">
            <div class="text absolute">
              <h3>各顯才能</h3>
              <p>希瑪醫療網羅不同學科的人才，令團隊更多元創新，抱著以客戶為中心的共同目標，為顧客提供度身訂造的專科醫療服務。</p>
            </div>
          </li>

          <li class="md:ml-auto relative">
            <img src="../../assets/images/joinus/section2_3.jpg" alt="">
            <div class="text absolute">
              <h3>熱誠投入</h3>
              <p>希瑪醫療相信我們的人才優勢在於團隊合作，對工作充滿熱誠和全情投入，更對美好生活滿懷熱情。我們致力為員工締造開心工作環境，達致工作生活平衡及提升生產力。</p>
            </div>
          </li>
        </ul>

      </section>
      <section class="section3">
        <div class=" text_box text-center">我們希望吸納更多醫護及不同學科的專才，<br>
          加入希瑪醫療，盡展所長！</div>
        <div>
          加入我們
          <span><i class="fa fa-angle-right "></i></span>
        </div>
      </section>

    </section>
    <section class="foot">
      <Footer />
    </section>

  </div>
</template>

<script>

import "../../assets/css/joinus/common.css"
import "../../assets/css/joinus/mb.css"
import "../../assets/css/joinus/pc.css"


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