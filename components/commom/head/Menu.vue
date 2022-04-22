<template>
  <div class="menu">
    <div class="section1"> <div class="text">希瑪眼科醫療控股有限公司 香港聯交所 上市編號03309.HK</div> </div>
    <div class="section2 flex justify-between items-center">
      <div class="md:flex-1">
        <nuxt-link to="/"><img class="logo" src="../../../assets/images/common/Logo.svg" alt=""></nuxt-link>
      </div>

      <!-- pc navbar -->
      <ul class="nav flex-1 hidden  md:flex justify-between md:h-full">
        <li v-for="(navItem,index) in navList " :key="index" class="nav_item md:flex md:items-center">
          <nuxt-link :to="navItem.link" class="main_nav">
            <div class="mian_nav_text  font-black">{{navItem.main_nav}}</div>
          </nuxt-link>
          <ul class="child_nav  flex-col gap-2 sm:hidden" v-if=" 0 !== navItem.child_list.length ">
            <li v-for="(childItem,index) in navItem.child_list " :key="index">
              <nuxt-link :to="childItem.link">{{childItem.child_item}}</nuxt-link>
            </li>
          </ul>
        </li>
        <li class="nav_item md:flex md:items-center"><img src="../../../assets/images/common/Frame.svg" alt="">
        <ul class="child_nav navbar_language">
          <li><nuxt-link to="">中文</nuxt-link> </li>
          <li><nuxt-link to="">English</nuxt-link></li>
        </ul>
        </li>
      </ul>

      <!-- mb navbr -->
      <div class=" mb_bar_bt md:hidden">
        <div class="bt" v-show="!navIsShow" @click="showNavbar"><i class="fa fa-bars "></i></div>
        <div class="bt" v-show="navIsShow" @click="closeNavbar"><i class="fa fa-times "></i></div>
      </div>

      <div class="mb_navbar absolute w-full  flex md:hidden" v-show="navIsShow">
        <ul class=" mb_nav  bg-white flex flex-col gap-5 ">
          <li v-for="(navItem,index) in navList " :key="index" class="nav_item md:flex ">
            <nuxt-link :to="navItem.link" class="main_nav">
              <div class="mian_nav_text  font-black">{{navItem.main_nav}}</div>
              <ul class="child_nav  flex-col gap-2 " v-if=" 0 !== navItem.child_list.length ">
              <li v-for="(childItem,index) in navItem.child_list " :key="index">
                <nuxt-link :to="childItem.link">{{childItem.child_item}}</nuxt-link>
              </li>
            </ul>
            </nuxt-link>
            
          </li>
          <a href=""><img src="../../../assets/images/common/Frame.svg" alt=""></a>

        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      navList: [
        {
          main_nav: "關於希瑪",
          link: "/",
          child_list: [
            {
              child_item: "業務介紹",
              link: "/about/introduction"
            }, {
              child_item: "發展里程碑",
              link: "/about/history"
            }, {
              child_item: "獎項及嘉許",
              link: "/about/award"
            }, {
              child_item: "地域覆蓋",
              link: "/about/region"
            },
          ]
        }, {
          main_nav: "集團業務",
          link: "",
          child_list: [
            {
              child_item: "希瑪眼科中心",
              link: "/business/cmereye"
            }, {
              child_item: "希瑪牙科中心",
              link: "/business/cmerdental"
            }, {
              child_item: "希瑪家庭醫學中心",
              link: "/business/cmerfamily"
            }, {
              child_item: "愛瑪醫美",
              link: "/business/ameraesthetics"
            }, {
              child_item: "希瑪中西腫瘤專科",
              link: "/business/cmeroncology"
            }, {
              child_item: "腸胃科",
              link: "/business/stomach"
            }, {
              child_item: "希瑪體檢中心",
              link: "/business/cmerrapidtest"
            }
          ]
        }, {
          main_nav: "抗疫專區",
          link: "/anti",
          child_list: []
        }, {
          main_nav: "加入我們",
          link: "/joinus",
          child_list: []
        }, {
          main_nav: "聯絡我們",
          link: "/contact",
          child_list: []
        },
      ],
      navIsShow: false,
    };
  },
  methods: {
    showNavbar() {
      this.navIsShow = true;
    },
    closeNavbar() {
      this.navIsShow = false;
    }
  }
}
</script>

<style scoped>
/* common */
.section1 {
  background: linear-gradient(0deg, #868686, #868686), #949494;
  color: white;
  text-align: center;
  margin: 0 auto;
}
.section2 {
  color: #64acc6;
  margin: 0 auto;
}
.section2 .nav li {
  position: relative;
}
.section2 .nav li:hover {
  color: #f09038;
}
.section2 .nav li::before {
  content: " ";
  position: absolute;
  border-bottom: 2px solid #f09038;
}
.section2 .nav li::before {
  -webkit-transition: width 0.5s ease-in-out;
  -moz-transition: width 0.5s ease-in-out;
  -ms-transition: width 0.5s ease-in-out;
  -o-transition: width 0.5s ease-in-out;
  transition: width 0.5s ease-in-out;
}
.section2 .nav .nav_item {
  position: relative;
}
.section2 .nav .nav_item .child_nav {
  position: absolute;
  z-index: 1;
  background: rgba(255, 255, 255, 0.8); backdrop-filter: blur(3px)  ;
  color: #f09038;
  align-items: start;
  justify-content: center;display: none;
}
.section2 .nav .nav_item:hover .child_nav{
  display: flex;
}
.section2 .nav .nav_item .child_nav li {
  display: inline-block;
}
/* pc */
@media only screen and (min-width: 768px) {
  .section1 {
    width: 93vw;
    height: 2.5vw;
    line-height: 2.5vw;
  }
  .section2 {
    width: 90vw;
    margin: 0 auto;
    height: 5vw;
  }
  .section2 .nav li {
    position: relative;
  }
  .section2 .nav li::before {
    width: 0%;
    bottom: 1.4vw;
    left: -5%;
  }
  .section2 .nav .child_nav li::before {
    left: 0;
    bottom: -0.5vw;
  }
  .section2 .nav .nav_item:hover::before {
    width: 110%;
  }
  .section2 .nav .child_nav li:hover::before {
    width: 100%;
  }
  .section2 .nav .nav_item .child_nav {
    top: 3.6vw;
    font-size: 0.8vw;
    width: 12vw;
    padding: 1vw 0vw 0.5vw 1.2vw;
  }
  .section2 .nav .nav_item .child_nav li {
    margin-bottom: 1vw;
  }
  .navbar_language{right: 0;width: auto !important;flex-flow: column;padding: 1vw 0.5vw;}
  .navbar_language li{display: block !important;}
}

/* md   */

/* mobile */
@media only screen and (max-width: 768px) {
  .fa-remove:before,
  .fa-close:before,
  .fa-times:before {
    content: "\f00d" !important;
  }

  .section1 {
    width: 90vw;
    font-size: 12px;
    padding: 5px 0;
  }
  .section1 .text{transform: scale(.8);}
  .section2 {
    width: 90vw;
    margin: 0 auto;
    padding: 10px 0;
  }

  .section2 .logo {
    width: 13vw;
  }
  .section2 .nav li {
    position: relative;
  }
  .section2 .nav li::before {
    width: 0%;
    bottom: -0.5vw;
    left: -5%;
  }
  .section2 .nav .child_nav li::before {
    left: 0;
  }
  .section2 .nav .nav_item:hover::before {
    width: 110%;
  }
  .section2 .nav .child_nav li:hover::before {
    width: 100%;
  }
  .section2 .nav .nav_item .child_nav {
    top: 2vw;
    font-size: 0.8vw;
    width: 12vw;
    padding: 1vw 0vw 0.5vw 1.2vw;
  }
  .section2 .nav .nav_item .child_nav li {
    margin-bottom: 1vw;
  }

  .mb_navbar {
    margin-left: -10vw;
    top: 10vh;
    height: 90vh;
    width: 105vw;z-index: 9999;
  }
  .mb_navbar .mb_nav {
    width: 100%;text-align: center;padding-top: 30px;height: calc(100vh - 80px);
  }
  .mb_navbar .mb_nav>a{display: none;}
  .mb_navbar .bg-black{backdrop-filter: blur(3px)  ;}
  .mb_bar_bt .bt {
    font-size: 25px;
    -webkit-text-stroke: 1px #fff;
  }
 .mb_navbar .mb_nav .nav_item:nth-child(1) .mian_nav_text, .mb_navbar .mb_nav .nav_item:nth-child(2) .mian_nav_text{display: inline-block; padding-bottom: 7px; margin-bottom: 7px; border-bottom: 1px solid;}
  .mb_navbar .mb_nav .nav_item{margin-bottom: 10px;}
  .mb_navbar .mb_nav .nav_item  .mian_nav_text{font-size: 24px;}
    .mb_navbar .mb_nav .nav_item  .child_nav a{font-size: 18px;}
  .mb_navbar .mb_nav .nav_item >.child_nav  {display: none;}
}
</style>