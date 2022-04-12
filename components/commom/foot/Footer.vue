<template>
  <div class="footer">
    <ul class="nav flex-1  md:flex justify-between ">
      <li v-for="(navItem,index) in navList " :key="index" class="nav_item md:flex flex-col">
        <nuxt-link :to="navItem.link" class="main_nav">
          <div class="mian_nav_text  font-black">{{navItem.main_nav}}</div>
        </nuxt-link>
        <ul class="child_nav  flex-col gap-2 ">
          <li v-for="(childItem,index) in navItem.child_list " :key="index">
            <nuxt-link :to="childItem.link">{{childItem.child_item}}</nuxt-link>
          </li>
        </ul>
      </li>
    </ul>
    <div class="contact flex items-center justify-center font-black">
      聯絡 <img src="../../../assets/images/common/foot_cmer.svg" alt="">我們
    </div>
    <div class="footer_finally flex items-center justify-between">
      <div>條款細則<span>@2022 希瑪醫療有限公司 版權所有 </span></div>
      <img src="../../../assets/images/common/Logo.svg" alt="">
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
          link: "",
          child_list: [
            {
              child_item: "業務介紹",
              link: ""
            }, {
              child_item: "里程碑",
              link: ""
            }, {
              child_item: "傑出成就",
              link: ""
            }, {
              child_item: "地域覆蓋",
              link: ""
            },
          ]
        }, {
          main_nav: "集團業務",
          link: "",
          child_list: [
            {
              child_item: "希瑪眼科中心",
              link: ""
            }, {
              child_item: "微笑激光矯視中心",
              link: ""
            }, {
              child_item: "視光中心",
              link: ""
            }, {
              child_item: "視光中心",
              link: ""
            }, {
              child_item: "愛瑪醫美",
              link: ""
            }
          ]
        }, {
          main_nav: "診症須知",
          link: "",
          child_list: [
            {
              child_item: "",
              link: ""
            },
          ]
        }, {
          main_nav: "抗疫專區",
          link: "",
          child_list: []
        }, {
          main_nav: "加入我們",
          link: "",
          child_list: [
            {
              child_item: "",
              link: ""
            },
          ]
        }, {
          main_nav: "聯絡我們",
          link: "",
          child_list: [
            {
              child_item: "",
              link: ""
            },
          ]
        },
      ]
    };
  },
  created() { },
  methods: {}
};
</script>

<style scoped>
.footer {
  margin-top: 10vw;
  background: #80c5de;
}
.footer .nav {
  width: 71vw;
  margin: 0 auto;
  color: #fff;
  padding: 5vw 0;
}
.footer .child_nav {
  margin-top: 2vw;
}
.footer .child_nav li {
  margin: 0.5vw 0;
}
.contact {
  background: #64acc6;
  color: #fff;
  padding: 2vw 0;
  font-size: 2vw;
}
.contact img {
  width: 5vw;
}
.footer_finally{
    background: #fff;
    height: 5vw;
    padding:0 14vw;
    font-size: 0.8vw;
}
.footer_finally span{
    margin-left:4vw;
}
</style>