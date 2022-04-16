<template>
  <div>

    <section class="head">
      <Menu />
      <div class="banner"></div>
      <div class="scroll_down flex-col items-center justify-center hidden md:flex"><span class=" font-black">Scroll</span><img src="@/assets/images/common/down.svg" alt=""></div>
    </section>

    <section class="mainContent">
      <div class="award flex justify-end">
        <img ref="title_img" :class="{deleteFixd:isDeleteFixd}" class="title_img" src="../assets/images/home/banner_txt.svg" alt="">
        <div class="text">優質港式醫療服務品牌。<br>打造希瑪醫療成為全國性的</div>
        <div class="blue_box">
          <h3 class=" font-black">
            我們的使命
          </h3>
          <p class=" text-justify">利用希瑪醫療的香港醫療基因和品牌，由眼科開始逐步發展至多個專科領域，為粵港澳大灣區以至內地其他地區的居民提供優質的中高端專科醫療服務。</p>
          <a href="" class=" flex items-center font-black wow animate__animated animate__fadeInLeftBig">獎項及嘉許 <div><i class=" ml-5 fa fa-angle-right"></i></div></a>
        </div>
      </div>

      <div class="business">
        <h2 class="flex items-center justify-center font-black wow animate__animated animate__fadeInUp" data-wow-duration="1s" data-wow-delay="0s">希瑪 <img src="../assets/images/home/title1.svg" alt=""> 業務</h2>
        <ul class="flex flex-wrap justify-between items-center md:justify-center">
          <li v-for="(businessIten,index) in businessList" :key="index" class=" wow animate__animated animate__fadeInDown" :data-wow-delay="'1.'+index+'s'">
            <div class="img"><img :src="businessIten.img" alt=""></div>
            <div class="des flex font-black items-center "><img :src="businessIten.icon" alt=""><span>{{businessIten.des}}</span></div>
          </li>
        </ul>
      </div>

      <div class="anti ">
        <nuxt-link to=" ">
          <div class="anti_box  wow animate__animated animate__fadeInUp" data-wow-duration="0.8s">
            <img src="../assets/images/home/anti_bg.jpg" alt="">
            <span>/抗疫專區/</span>
          </div>
        </nuxt-link>
      </div>

      <div class="join flex justify-between  md:justify-end">
        <div class="join_img  ">
          <img class="img" src="../assets/images/home/join_bg.jpg" alt="">
          <div class="join_link flex flex-col  items-center justify-center wow animate__animated  animate__fadeInUp">
            <span class="font-bold">/加入我們/</span>
            <a href="" class="more_link">更多 <span class="fa_right"><i class="fa fa-angle-right "></i></span> </a>
          </div>
        </div>
        <div class="join_side_text  font-black wow animate__animated animate__fadeInLeft"><span>WORK WITH US</span></div>
      </div>

      <div class="about_box">
        <div class="about flex justify-between md:justify-start">
          <div class="about_side_text  font-black wow animate__animated animate__fadeInRight"><span>ABOUT US</span></div>
          <div class="about_img  ">
            <img class="img" src="../assets/images/home/about_bg.png" alt="">
            <div class="about_link flex flex-col  items-center justify-center wow animate__animated  animate__fadeInUp">
              <span class=" font-bold">/關於希瑪/</span>
              <a href="" class="more_link">更多 <span class="fa_right"><i class="fa fa-angle-right "></i></span> </a>
            </div>
          </div>
        </div>

        <div class="blue_box hidden md:block">
          <a href="">
            <div class="link flex ">
              <div class="down_blue flex items-center justify-center">
                <img src="../assets/images/common/down_blue.svg" alt="">
              </div>
              <img src="../assets/images/home/choise_white.svg" alt="">
            </div>
          </a>

        </div>

      </div>

      
      <!-- 
     

     

     

    

      <div class="puzzle mt-56">
        <div class="flex items-center justify-center relative">
          <div class="puItem pu1"></div>
          <div class="puItem pu2"></div>
          <div class="puItem pu3"></div>
        </div>
        <div class="flex items-center justify-center relative">
          <div class="puItem pu4"></div>
          <div class="puItem pu5"></div>
          <div class="puItem pu6"></div>
          <div class="puItem pu7"></div>
        </div>
      </div>-->
    </section>

    <section class="foot">
      <Footer />
    </section>

  </div>
</template>

<script>

if (process.browser) { // 在这里根据环境引入wow.js
  var { WOW } = require('wowjs')
}

import "@/assets/css/home/common.css"
import "@/assets/css/home/pc.css"
import "@/assets/css/home/mb.css"

import Menu from "@/components/commom/head/Menu.vue"
import Footer from "@/components/commom/foot/Footer.vue"

import InnerSlider from "../components/commom/slider/InnerSlider.vue"
export default {
  components: { Menu, Footer, InnerSlider },
  data() {
    return {
      businessList: [
        {
          img: require('@/assets/images/home/business1.jpg'),
          des: '希瑪眼科',
          icon: require('@/assets/images/home/bu_icon1.svg')
        },
        {
          img: require('@/assets/images/home/business2.jpg'),
          des: '腸胃科',
          icon: require('@/assets/images/home/bu_icon2.svg')
        },
        {
          img: require('@/assets/images/home/business3.jpg'),
          des: '希瑪中西腫瘤專科',
          icon: require('@/assets/images/home/bu_icon3.svg')
        },
        {
          img: require('@/assets/images/home/business4.jpg'),
          des: '希瑪牙科',
          icon: require('@/assets/images/home/bu_icon4.svg')
        },
        {
          img: require('@/assets/images/home/business5.jpg'),
          des: '希瑪體檢中心',
          icon: require('@/assets/images/home/bu_icon5.svg')
        },
        {
          img: require('@/assets/images/home/business6.jpg'),
          des: '希瑪家庭醫學中心',
          icon: require('@/assets/images/home/bu_icon6.svg')
        },
        {
          img: require('@/assets/images/home/business7.jpg'),
          des: '愛瑪醫美',
          icon: require('@/assets/images/home/bu_icon7.svg')
        },
      ],
      isDeleteFixd: false,

    }

  },

  mounted() {
    if (process.browser) {  // 在页面mounted生命周期里面 根据环境实例化WOW
      new WOW({
        live: false,
        offset: 0
      }).init()
    }
    window.addEventListener('scroll', this.windowScroll)
  },

  methods: {
    windowScroll() {
      let scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop;
      if (scrollTop >= 592) {
        console.log(11);
        this.isDeleteFixd = true;
      } else {
        this.isDeleteFixd = false;
      }
    }

  },



}
</script>

<style>
</style>