<template>
  <div>

    <section class="head">
      <Menu />
      <div class="banner"></div>
      <div class="scroll_down flex flex-col items-center justify-center"><span class=" font-black">Scroll</span><img src="../assets/images/common/down.svg" alt=""></div>
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
        <ul class="flex flex-wrap items-center justify-center">
          <li v-for="(businessIten,index) in businessList" :key="index" class=" wow animate__animated animate__fadeInDown" :data-wow-delay="'1.'+index+'s'">
            <div class="img"><img :src="businessIten.img" alt=""></div>
            <div class="des flex font-black "><img :src="businessIten.icon" alt=""><span>{{businessIten.des}}</span></div>
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

      <div class="join flex  justify-end">
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
        <div class="about flex justify-start">
          <div class="about_side_text  font-black wow animate__animated animate__fadeInRight"><span>ABOUT US</span></div>
          <div class="about_img  ">
            <img class="img" src="../assets/images/home/about_bg.png" alt="">
            <div class="about_link flex flex-col  items-center justify-center wow animate__animated  animate__fadeInUp">
              <span class=" font-bold">/關於希瑪/</span>
              <a href="" class="more_link">更多 <span class="fa_right"><i class="fa fa-angle-right "></i></span> </a>
            </div>
          </div>
        </div>

        <div class="blue_box">
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
      </div>
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
import Menu from "@/components/commom/head/Menu.vue"
import Footer from "@/components/commom/foot/Footer.vue"
export default {
  components: { Menu, Footer },
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


<style scoped>
.banner {
  background-image: url(../assets/images/home/banner_bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  width: 85vw;
  margin: 0 auto;
  height: 37vw;
  background-position: bottom;
}
.award .title_img {
  width: 18vw;
  position: fixed;
  top: 30.5vw;
  left: 9vw;
}
.award .deleteFixd {
  position: absolute;
  top: 60vw;
}

.scroll_down {
  text-align: center;
  color: rgba(240, 144, 56, 1);
  margin-top: 1vw;
}

.award {
  margin: 5vw 0;
  font-size: 1.2vw;
}
.award .text {
  writing-mode: vertical-lr;
  line-height: 2.5vw;
}
.award .blue_box {
  color: #ffff;
  background: #80c5de;
  width: 30vw;
  height: 24vw;
  padding: 2vw 5vw 3vw 6vw;
  margin-left: 1vw;
}
.award .blue_box h3 {
  text-align: right;
  margin-bottom: 1vw;
}
.award .blue_box a {
  margin-top: 5vw;
  transition: all 0.5s;
}
.award .blue_box a:hover {
  transform: scale(1.2);
}
.award .blue_box a img {
  width: 0.5vw;
  margin-left: 1vw;
}

.business {
  width: 71vw;
  margin: 5vw auto;
}
.business h2 {
  color: #80c5de;
  font-size: 2.7vw;
}
.business h2 img {
  width: 5vw;
}
.business ul li {
  width: 15.7vw;
  margin: 2vw 1vw;
  transition: all 0.5s;
}
.business ul li:hover {
  box-shadow: 12px 12px 0px 0px #f09038;
  transform: translate(-12px, -12px);
}
.business ul li .img img {
  width: 100%;
}
.business ul li .des {
  border: 1px solid #a5a5a5;
  border-top: none;
  padding: 1.5vw;
  font-size: 1.2vw;
}
.business ul li .des img {
  margin-right: 0.5vw;
  width: 1.5vw;
}
.anti {
  margin: 5vw auto;
  position: relative;
  padding-top: 1vw;
}
.anti::before {
  content: " ";
  position: absolute;
  width: 32vw;
  height: 32vw;
  background: #80c5de;
  top: 0;
  z-index: 0;
}
.anti .anti_box {
  width: 71vw;
  margin: 0 auto;
  background: #000;
  position: relative;
  transition: all 0.5s;
}

.anti img {
  position: relative;
  width: 71vw;
  margin: 5vw auto;
  z-index: 10;
  transition: all 0.5s;
}
.anti .anti_box:hover img {
  opacity: 0.6;
  filter: alpha(opacity=60);
}
.anti span {
  position: absolute;
  top: 38%;
  left: 7%;
  z-index: 11;
  font-size: 6vw;
  font-weight: 900;
  color: white;
  letter-spacing: 6.5vw;
  white-space: nowrap;
}

.join {
  margin-top: 10vw;
  padding-right: 2vw;
}
.join .join_side_text,
.about .about_side_text {
  writing-mode: vertical-lr;
  color: #f09038;
  font-size: 3.6vw;
}
.join .join_img {
  position: relative;
}
.join .join_img .img {
  width: 58vw;
}
.join .join_img .join_link {
  position: absolute;
  background: #ffff;
  right: 0;
  bottom: 0;
  width: 16vw;
  height: 16vw;
}
.join .join_img .join_link > span,
.about .about_img .about_link > span {
  font-size: 2vw;
}

.about {
  margin-top: 6vw;
  padding-left: 2vw;
}
.about .about_img {
  position: relative;
  z-index: 1;
}
.about .about_img .img {
  width: 57vw;
}
.about .about_img .about_link {
  position: absolute;
  background: #ffff;
  left: 0;
  bottom: 0;
  width: 16vw;
  height: 16vw;
}
.about_box {
  position: relative;
}
.about_box .blue_box {
  position: absolute;
  background: #80c5de;
  right: 0;
  top: 10vw;
  width: 39vw;
  z-index: 0;
  height: 25vw;
}

.about_box .blue_box .down_blue {
  width: 1.5vw;
  height: 1.5vw;
  background: #fff;
  border-radius: 100%;
  margin-top: 0.5vw;
  margin-right: 0.5vw;
}
.about_box .blue_box .down_blue img {
  width: 0.8vw;
  margin-top: 0.2vw;
}

.about_box .blue_box .link {
  position: absolute;
  right: 8vw;
  bottom: 3vw;
}

.puzzle .puItem {
  background-repeat: no-repeat;
  background-size: contain;
  width: 5vw;
  height: 5vw;
}

.puzzle .pu1 {
  background-image: url(../assets/images/home/Puzzle1.png);
}
.puzzle .pu1:hover {
  background-image: url(../assets/images/home/Puzzle1a.png);
}

.puzzle .pu2 {
  background-image: url(../assets/images/home/Puzzle2.png);
}
.puzzle .pu2:hover {
  background-image: url(../assets/images/home/Puzzle2a.png);
}

.puzzle .pu3 {
  background-image: url(../assets/images/home/Puzzle3.png);
}
.puzzle .pu3:hover {
  background-image: url(../assets/images/home/Puzzle3a.png);
}

.puzzle .pu4 {
  background-image: url(../assets/images/home/Puzzle4.png);
}
.puzzle .pu4:hover {
  background-image: url(../assets/images/home/Puzzle4a.png);
}

.puzzle .pu5 {
  background-image: url(../assets/images/home/Puzzle5.png);
}
.puzzle .pu5:hover {
  background-image: url(../assets/images/home/Puzzle5a.png);
}

.puzzle .pu6 {
  background-image: url(../assets/images/home/Puzzle6.png);
}
.puzzle .pu6:hover {
  background-image: url(../assets/images/home/Puzzle6a.png);
}

.puzzle .pu7 {
  background-image: url(../assets/images/home/Puzzle7.png);
}
.puzzle .pu7:hover {
  background-image: url(../assets/images/home/Puzzle7a.png);
}
</style>
