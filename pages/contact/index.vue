<template>
  <div>
      <Menu />
     <div class="banner">
         <img src="@/assets/images/about/banner_contact.jpg" alt="" srcset="">
         <div class="banner_txt">
               <span>聯絡我們</span>
               <p>Contact Us/</p>
         </div>
     </div>


<div class="contact_container  ">

    <table class="table">
        <tbody>
            <tr>
                <td><div class="icon"><img src="@/assets/images/about/contact/c1.svg" alt="" srcset=""></div> +852 3997 3266</td>
            </tr>
            <tr>
                <td><div class="icon"><img src="@/assets/images/about/contact/c2.svg" alt="" srcset=""></div> +852 3996 8212</td>
            </tr>
            <tr>
                <td><div class="icon"><img src="@/assets/images/about/contact/c3.svg" alt="" srcset=""> </div>info@hkcmer.com</td>
            </tr>
            <tr>
                <td><div class="icon"><img src="@/assets/images/about/contact/c4.svg" alt="" srcset=""></div> 中環畢打街1-3號中建大廈1535室</td>
            </tr>
        </tbody>
    </table>
<div class="h-100"></div>
    <table class="table table_blue">
        <tbody>
            <tr>
                <td scope="row">希瑪家庭醫學中心 </td>
                <td> <div class="icon"><img src="@/assets/images/about/contact/c5.svg" alt="" srcset=""></div>2602 2771</td>
            </tr>
            <tr>
                <td scope="row">希瑪體檢中心 </td>
                <td> <div class="icon"><img src="@/assets/images/about/contact/c5.svg" alt="" srcset=""></div>???? ????</td>
            </tr>
            <tr>
                <td scope="row">腸胃科 </td>
                <td> <div class="icon"><img src="@/assets/images/about/contact/c5.svg" alt="" srcset=""></div>???? ????</td>
            </tr>
            <tr>
                <td scope="row">希瑪中西腫瘤專科 </td>
                <td> <div class="icon"><img src="@/assets/images/about/contact/c6.svg" alt="" srcset=""></div>www.cmeroncology.com/contact</td>
            </tr>
            <tr>
                <td scope="row">希瑪牙科中心 </td>
                <td> <div class="icon"><img src="@/assets/images/about/contact/c6.svg" alt="" srcset=""></div>www.cmerdental.com/contact</td>
            </tr>
            <tr>
                <td scope="row">希瑪眼科中心 </td>
                <td> <div class="icon"><img src="@/assets/images/about/contact/c6.svg" alt="" srcset=""></div>www.hkcmereye.com/contact</td>
            </tr>
            <tr>
                <td scope="row">希瑪微笑矯視中心 </td>
                <td> <div class="icon"><img src="@/assets/images/about/contact/c6.svg" alt="" srcset=""></div>www.cmersmile.com/contact-us</td>
            </tr>
            <tr>
                <td scope="row">希瑪眼科視光中心 </td>
                <td> <div class="icon"><img src="@/assets/images/about/contact/c6.svg" alt="" srcset=""></div>www.cmervision.com/about-us/contact-us</td>
            </tr>
            <tr>
                <td scope="row">愛瑪醫美 </td>
                <td> <div class="icon"><img src="@/assets/images/about/contact/c6.svg" alt="" srcset=""></div>www.ameraesthetics.com/contact</td>
            </tr>
        </tbody>
    </table>

</div>

     
      <Footer />
  </div>
</template>

<style scoped>
/* mobile  */
@media screen  and (max-width:768px) {
.h-100{height: 100px;}   
.banner{ position: relative;}
.banner img{width: 100%; height: 100%;object-fit: cover;}
.banner_txt{position: absolute;top: 50%;left: 30%;transform: translate(-50%,-50%);}
.banner_txt span{ font-size: 30px; letter-spacing: 0.2em; color: #404040;}
.banner_txt p{ font-size: 2.2vw; letter-spacing: 0.2em; color: #fff;text-indent: 0;}
.contact_container{max-width: 100px;margin: 50px auto;margin-left: -15px;margin-right: -15px;}
.contact_container .table{width: 100%;border: 4px solid #F09038;border-left: none;border-right: none;}
.contact_container .table tr td{display: flex;justify-content: flex-start;align-items: center;padding: 20px 35px;font-size: 20px;letter-spacing: 0.15em;}
.contact_container .table tr td img{display: block;margin: auto;}
.contact_container .table tr {border-bottom:2px  solid  #F09038;}
.contact_container .table .icon{min-width: 50px;text-align: center;margin-right: 15px;}
.contact_container .table_blue,.contact_container .table_blue tr{border-color: #80C5DE !important;}
.contact_container .table_blue tr{display: flex;}
.contact_container .table_blue tr td:nth-child(1){width: 30%;}
.contact_container .table_blue tr td:nth-child(2){width: 70%;}

}
/* mobile end */

/* pc */
@media screen  and (min-width:768px) {
.h-100{height: 100px;}   
.banner{height:  calc(100vh - 86.7px);background: unset;position: relative;}
.banner img{width: 100%; height: 100%;object-fit: cover;}
.banner_txt{position: absolute;top: 50%;left: 15%;transform: translate(-50%,-50%);}
.banner_txt span{ font-size: 3vw; letter-spacing: 0.2em; color: #404040;}
.banner_txt p{ font-size: 2.2vw; letter-spacing: 0.2em; color: #fff;text-indent: 0;}
.contact_container{max-width: 53.2vw;margin: 100px auto;}
.contact_container .table{width: 100%;border: 4px solid #F09038;border-left: none;border-right: none;}
.contact_container .table tr td{display: flex;justify-content: flex-start;align-items: center;padding: 20px 35px;font-size: 20px;letter-spacing: 0.15em;}
.contact_container .table tr td img{display: block;margin: auto;}
.contact_container .table tr {border-bottom:2px  solid  #F09038;}
.contact_container .table .icon{min-width: 50px;text-align: center;margin-right: 15px;}
.contact_container .table_blue,.contact_container .table_blue tr{border-color: #80C5DE !important;}
.contact_container .table_blue tr{display: flex;}
.contact_container .table_blue tr td:nth-child(1){width: 30%;}
.contact_container .table_blue tr td:nth-child(2){width: 70%;}
}
/* pc end */

</style>

<script>

import Menu from "@/components/commom/head/Menu.vue"
import Footer from "@/components/commom/foot/Footer.vue"
export default {
  components: { Menu, Footer },
  data() {
    return {
    
    };
  },
  created() { },
  methods: {}
};
</script>

