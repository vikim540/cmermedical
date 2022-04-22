<template>
  <div>

    <section class="head">
      <Menu />
      <div class="banner"></div>
      <div class="scroll_down flex-col items-center justify-center hidden md:flex"><span class=" font-black">Scroll</span>
      <img class="mt-2" src="@/assets/images/common/down.svg" alt=""></div>
    </section>

    <section class="mainContent">
      <div class="award flex justify-end">
<div ref="title_img" :class="{deleteFixd:isDeleteFixd}" class="title_img">
    <div class="title_rel">
       <p>希</p>
 <p>望見美好</p>
 <div class="title_center"><p>Our vision <br> for a better future</p>  </div>
      </div>  
</div>


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
          <div class="anti_box  wow animate__animated animate__fadeInUp overflow-hidden  " data-wow-duration="0.8s">
            <img src="../assets/images/home/anti_bg.jpg" alt="">
            <img src="../assets/images/home/AntiCovid.svg" alt="">
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

       <div class="puzzle mt-56">
        <div class="flex items-center justify-center relative">
          <div class="puItem pu1"><div class="puItem_rel"><div class="text">希瑪 <br>家庭醫學中心</div><img src="../assets/images/home/Puzzle1.png" alt=""></div></div>
          <div class="puItem pu2"><div class="puItem_rel"><div class="text">希瑪 <br>體檢中心</div> <img src="../assets/images/home/Puzzle2.png" alt=""></div></div>
          <div class="puItem pu3"><div class="puItem_rel"><div class="text">腸胃科</div><img src="../assets/images/home/Puzzle3.png" alt=""></div></div>
          <div class="puItem pu4"><div class="puItem_rel"><div class="text">愛瑪醫美</div><img src="../assets/images/home/Puzzle4.png" alt=""></div></div>
          <div class="puItem pu5"><div class="puItem_rel"><div class="text">希瑪眼科</div><img src="../assets/images/home/Puzzle5.png" alt=""></div></div>
          <div class="puItem pu6"><div class="puItem_rel"><div class="text">希瑪牙科</div><img src="../assets/images/home/Puzzle6.png" alt=""></div></div>
          <div class="puItem pu7"><div class="puItem_rel"><div class="text">希瑪<br>中西腫瘤專科</div><img src="../assets/images/home/Puzzle7.png" alt=""></div></div>
        <div class="puzzle_left"><img src="../assets/images/home/PuzzleLeft.svg" alt="" srcset=""></div>  
        </div>
        
      </div> 
    </section>

    <section class="foot">
      <Footer />

<div class="scroll_top rotate-90 inline-block" @click="toTop"><i class="fa fa-caret-left"></i> TOP</div> 

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
      gotop: false,

    }

  },

  mounted() {
    if (process.browser) {  // 在页面mounted生命周期里面 根据环境实例化WOW
      new WOW({
        live: false,
        offset: 0
      }).init()
    }
    window.addEventListener('scroll', this.windowScroll, true)
  },

  methods: {
    windowScroll() {
      let scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop;
      let scrollHeight = document.documentElement.scrollHeight || document.body.scrollHeight;
      if (scrollTop >= 592) {
        console.log(11);
        this.isDeleteFixd = true;
      } else {
        this.isDeleteFixd = false;
      }
    },
    handleScroll() {
      let scrolltop = document.documentElement.scrollTop || document.body.scrollTop;
      scrolltop > 1000 ? (this.gotop = true) : (this.gotop = false);
    },
    toTop() {
      
      let top = document.documentElement.scrollTop || document.body.scrollTop;
      // 实现滚动效果 
      const timeTop = setInterval(() => {
        document.body.scrollTop = document.documentElement.scrollTop = top -= 50;
        if (top <= 0) {
          clearInterval(timeTop);
        }
      }, 10);

  },



},

}
</script>
 
<style scoped>
.business ul li{transition: all .3s ease-in !important;}
.business ul li:hover{box-shadow: 10px 10px 0 #F09038;transform: translate(-12px, -12px) !important;}

.scroll_down .font-black{animation: fade 0.8s ease-in-out alternate infinite;}
.scroll_down img{animation: fade 0.8s ease-in-out alternate infinite;animation-delay: 0.2s;}

.join .join_img::before{content: '////////';position: absolute;left: -10vw;top: -2.5vw;font-size: 3vw;color: #F09038;letter-spacing: 0.25em;}
.join .join_img::after{content: '////////';position: absolute;left: -26vw;top: -2.5vw;font-size: 3vw;color: #80C5DE;letter-spacing: 0.25em;}

@keyframes fade {
  from {
    opacity: 0;transform: translateY(0px);
  }
  to {
    opacity: 1;transform: translateY(10px);
  }
}

/* pc */
@media screen and (min-width:768px) {
.about_box .blue_box{right: 0;}  
.puzzle {position: relative;}
.puzzle .puItem{width: fit-content;height: auto;}
.puzzle .puItem img{visibility: hidden;}
.puzzle .flex{max-width: 80vw; margin: 0 auto;position: relative;min-height: 46.7vw;transform: scale(.8);}
.puzzle .flex::before{content: '';position: absolute;top: 0;left: 0;right: 0;bottom: 0;margin: auto; width: 8vw;height:4vw;background:url(../assets/images/home/Puzzlelogo.svg);transition: all .3s ease-in;background-size:auto  100% ;background-position: center;background-repeat: no-repeat;}
.anti img{margin: auto;}
.anti .anti_box{margin-top: 5vw;}
.puzzle .flex .puItem{position: absolute;top:0;left: 0;right: 0;margin: auto;background-position: center;}
.puzzle .flex .puItem:nth-child(1){left: -26.2vw; top: 2.35vw; width: 21vw; height: 21vw;}
.puzzle .flex .puItem:nth-child(2){    left: 0; right: 0; top: 0; width: 20vw; height: 16.6vw;}
.puzzle .flex .puItem:nth-child(3){ left: unset; right: 17.35vw; top: 2.5vw; width: 19.3vw; height: 19vw;}
.puzzle .flex .puItem:nth-child(4){    left: -29.35vw; right: 0; top: 18.25vw; width: 18vw; height: 19.5vw;}
.puzzle .flex .puItem:nth-child(5){   left: -14.7vw; right: 0; top: unset; bottom: 0.1vw; width: 22vw; height: 18.5vw;}
.puzzle .flex .puItem:nth-child(6){    left: 18.35vw; right: 0; top: 28.15vw; width: 18.5vw; height: 18.5vw;}
.puzzle .flex .puItem:nth-child(7){right: 16.75vw; left: unset; top: 16.5vw; width: 17.3vw; height: 21.2vw;}
.puzzle .puItem_rel{position: relative;width: 100%;height: 100%;}
.puzzle .puItem_rel .text{position: absolute;left: 0;right: 0;top: 0;bottom: 0;margin: auto;display: flex;justify-content: center;align-items: center;font-size: 1.5vw;text-align: center;color:#fff;}
.puzzle .flex .puItem:nth-child(1) .puItem_rel .text{margin-left: -1.5vw;margin-top: 0vw;}
.puzzle .flex .puItem:nth-child(2) .puItem_rel .text{margin-left: -2.5vw;margin-top: 0vw;}
.puzzle .flex .puItem:nth-child(3) .puItem_rel .text{margin-left: -1.5vw;margin-top: 0vw;}
.puzzle .flex .puItem:nth-child(4) .puItem_rel .text{margin-left: -0.5vw;margin-top:0vw;}
.puzzle .flex .puItem:nth-child(5) .puItem_rel .text{margin-left: 2.5vw;margin-top: 0vw;}
.puzzle .flex .puItem:nth-child(6) .puItem_rel .text{margin-left: -0.5vw;margin-top: 0vw;}
.puzzle .flex .puItem:nth-child(7) .puItem_rel .text{    margin-left: 2.5vw; margin-top: -2vw;}

.about_box .blue_box .link{align-items: flex-end;display: flex;}
.about .about_img::before{    position: absolute; content: '/////////////////'; color: #F09038; font-size: 2vw; bottom: -1vw; right: -14vw; letter-spacing: 0.25em;} 
.puzzle  .puzzle_left{    position: absolute;     bottom: -5vw; left: -5vw;max-width: 22vw;}

.scroll_top{position: fixed;color: #F09038; bottom: 2vw;right: 2vw;z-index: 999;width: 4vw;height: 2vw;display: flex;justify-content: center;align-items: center;transition: all .3s ease-in;cursor: pointer;}
.scroll_top:hover{background: #F09038;color: #fff;}
.scroll_top i{margin-right: 5px;}
.anti img:nth-child(2){position: absolute;    right: 9%; top: 20%;width: auto;height: auto;max-width: 8vw;}
.award .title_img{    height: 11.8vw; }
.award .title_img .title_rel{position: relative;width: 100%;height: 100%;}
.award .title_img .title_rel::before{width: 3vw;height: 5vw;content: '';right: 0;top: 0;background:unset;position: absolute;}
.award .title_img .title_rel .title_center{    position: absolute; top: -2vw; right: -1vw; left: 0; bottom: 0; margin: auto; display: flex; align-items: center; justify-content: center; color: #131313; text-align: right; transform: scale(0.8);}
.award .title_img .title_rel>p{font-size: 4vw;font-weight: bold; white-space: nowrap; line-height: 1.42;text-indent: 1vw;display: inline-block;background: #fff;padding: 0.4vw 0;}
.award .title_img .title_rel>p:nth-child(1){width: 79%;}
.award .title_img .title_rel .title_center p{font-family:'Metropolis';  font-weight: lighter; font-size: 1vw;position: relative;margin-top: 1vw;}
.award .title_img .title_rel>p:nth-child(2){padding-top: 0;}
.award .title_img .title_rel .title_center p::before{position: absolute;content: ' · ';font-weight: bold;       left: -5.8vw; bottom: -2.5vw;font-size: 3vw;}
.award .title_img.deleteFixd p{color: #F09038 !important;}
}


@media screen and (max-width:768px) {
/* div{overflow-x: hidden;}   */
.award{align-items: flex-end !important;}  
.banner{height:calc(100vh - 85px);background-position: center right 33%; background-size: auto 100%;}
.award .title_img{left: 9vw;}
.award .title_img{width: 40vw;bottom: 10vh;top: unset;position: absolute;}
.business ul li .des span{white-space: nowrap;}
.business ul li .des img{margin-right: 3px;}
body{overflow-y: hidden;}
.anti span{font-size: 30px !important;}
.anti img:nth-child(2){position: absolute;    right: 4%; top: 7%;width: auto;height: auto;max-width: 12vw;}
.award .title_img{    height: 11.8vw; }
.award .title_img .title_rel{position: relative;width: 100%;height: 100%;}
.award .title_img .title_rel::before{width: 3vw;height: 5vw;content: '';right: 0;top: 0;background:unset;position: absolute;}
.award .title_img .title_rel .title_center{    position: absolute; top: -2vw; right: -1vw; left: 0; bottom: 0; margin: auto; display: flex; align-items: center; justify-content: center; color: #131313; text-align: right; transform: scale(0.8);}
.award .title_img .title_rel>p{font-size: 30px;font-weight: bold; white-space: nowrap; line-height: 1.42;text-indent: 1vw;display: inline-block;background: #fff;padding: 0.4vw 0;}
.award .title_img .title_rel>p:nth-child(1){width: 79%;}
.award .title_img .title_rel .title_center p{font-family:'Metropolis';  font-weight: lighter; font-size: 1vw;position: relative;margin-top: 0.5vw;}
.award .title_img .title_rel .title_center p::before{position: absolute;content: ' · ';font-weight: bold;    left: -6.2vw; bottom: -2vw;font-size: 3vw;}
.award .title_img.deleteFixd p{color: #F09038 !important;}


.puzzle {position: relative;margin-top: 50px !important;padding-bottom: 20px;}
.puzzle .puItem{width: fit-content;height: auto;}
.puzzle .puItem img{visibility: hidden;}
.puzzle .flex{max-width: 80vw; margin: 0 auto;position: relative;min-height: 46.7vw; }
.puzzle .flex::before{content: '';position: absolute;top: 0;left: 0;right: 0;bottom: 0;margin: auto; width: 8vw;height:4vw;background:url(../assets/images/home/Puzzlelogo.svg);transition: all .3s ease-in;background-size:auto  100% ;background-position: center;background-repeat: no-repeat;}
.puzzle .flex .puItem{position: absolute;top:0;left: 0;right: 0;margin: auto;background-position: center;}
.puzzle .flex .puItem:nth-child(1){left: -26.2vw; top: 2.35vw; width: 21vw; height: 21vw;}
.puzzle .flex .puItem:nth-child(2){    left: 0; right: 0; top: 0; width: 20vw; height: 16.6vw;}
.puzzle .flex .puItem:nth-child(3){ left: unset; right: 17.35vw; top: 2.5vw; width: 19.3vw; height: 19vw;}
.puzzle .flex .puItem:nth-child(4){    left: -29.35vw; right: 0; top: 18.25vw; width: 18vw; height: 19.5vw;}
.puzzle .flex .puItem:nth-child(5){   left: -14.7vw; right: 0; top: unset; bottom: 0.1vw; width: 22vw; height: 18.5vw;}
.puzzle .flex .puItem:nth-child(6){    left: 18.35vw; right: 0; top: 28.15vw; width: 18.5vw; height: 18.5vw;}
.puzzle .flex .puItem:nth-child(7){right: 16.75vw; left: unset; top: 16.5vw; width: 17.3vw; height: 21.2vw;}
.puzzle .puItem_rel{position: relative;width: 100%;height: 100%;}
.puzzle .puItem_rel .text{position: absolute;left: 0;right: 0;top: 0;bottom: 0;margin: auto;display: flex;justify-content: center;align-items: center;font-size: 1.5vw;text-align: center;color:#fff;white-space: nowrap;transform: scale(0.7);}
.puzzle .flex .puItem:nth-child(1) .puItem_rel .text{margin-left: -1.5vw;margin-top: 0vw;}
.puzzle .flex .puItem:nth-child(2) .puItem_rel .text{margin-left: -2.5vw;margin-top: 0vw;}
.puzzle .flex .puItem:nth-child(3) .puItem_rel .text{margin-left: -1.5vw;margin-top: 0vw;}
.puzzle .flex .puItem:nth-child(4) .puItem_rel .text{margin-left: -0.5vw;margin-top:0vw;}
.puzzle .flex .puItem:nth-child(5) .puItem_rel .text{margin-left: 2.5vw;margin-top: 0vw;}
.puzzle .flex .puItem:nth-child(6) .puItem_rel .text{margin-left: -0.5vw;margin-top: 0vw;}
.puzzle .flex .puItem:nth-child(7) .puItem_rel .text{    margin-left: 2.5vw; margin-top: -2vw;}
.puzzle  .puzzle_left{    position: absolute;     bottom: -5vw; left: -5vw;max-width: 22vw;}

}


</style>