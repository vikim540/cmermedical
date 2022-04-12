<template>
  <div class="menu">
    <div class="section1"> 希瑪眼科醫療控股有限公司 香港聯交所 上市編號03309.HK </div>
    <div class="section2 flex justify-between items-center">
      <div class="flex-1"><img src="../../../assets/images/common/Logo.svg" alt=""></div>
      <ul class="nav flex-1  md:flex justify-between ">
        <li v-for="(navItem,index) in navList " :key="index" class="nav_item md:flex">
          <nuxt-link :to="navItem.link" class="main_nav">
            <div class="mian_nav_text  font-black">{{navItem.main_nav}}</div>
          </nuxt-link>
          <ul class="child_nav  flex-col gap-2 hidden" v-if=" 0 !== navItem.child_list.length ">
            <li v-for="(childItem,index) in navItem.child_list " :key="index">
              <nuxt-link :to="childItem.link">{{childItem.child_item}}</nuxt-link>
            </li>
          </ul>
        </li>
        <a href=""><img src="../../../assets/images/common/Frame.svg" alt=""></a>
      </ul>
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
            },{
              child_item: "希瑪中西腫瘤專科",
              link: "/business/cmeroncology"
            },{
              child_item: "腸胃科",
              link: "/business/stomach"
            },{
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
      ]
    };
  },
}
</script>

<style scoped>
.section1 {
  background: linear-gradient(0deg, #868686, #868686), #949494;
  color: white;
  text-align: center;
  width: 93vw;
  margin: 0 auto;
  height: 2.5vw;
  line-height: 2.5vw;
}
.section2 {
  color: #64acc6;
  width: 90vw;
  margin: 0 auto;
  height: 5vw;
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
  width: 0%;
  bottom: -0.5vw;
  left: -5%;
}
.section2 .nav .child_nav li::before {
  left: 0;
}
.section2 .nav li::before {
  -webkit-transition: width 0.5s ease-in-out;
  -moz-transition: width 0.5s ease-in-out;
  -ms-transition: width 0.5s ease-in-out;
  -o-transition: width 0.5s ease-in-out;
  transition: width 0.5s ease-in-out;
}
.section2 .nav .nav_item:hover::before {
  width: 110%;
}
.section2 .nav .child_nav li:hover::before {
  width: 100%;
}
.section2 .nav li:hover .child_nav {
  display: flex;
  align-items: start;
  justify-content: center;
}
.section2 .nav .nav_item {
  position: relative;
}
.section2 .nav .nav_item .child_nav {
  position: absolute;
  top: 2vw;
  z-index: 1;
  font-size: 0.8vw;
  background: rgba(255, 255, 255, 0.8);
  color: #f09038;
  width: 12vw;
  padding: 1vw 0vw 0.5vw 1.2vw;
}
.section2 .nav .nav_item .child_nav li {
  margin-bottom: 1vw;
  display: inline-block;
}
</style>