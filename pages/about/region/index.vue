<template>
      <div class="">
<Menu />
<div class="banner_region_box">
<div class="banner_region_bgpic"></div>
<div class="banner_region"> 
    <div class="banner_region_animatebg wow animate__animated animate__fadeBg" data-wow-duration="1s" data-wow-delay="0s"></div> 
    <div class="banner_about_text "><h1 class=" wow animate__animated animate__fadeInRight" data-wow-duration="1s" data-wow-delay="0.2s">地域覆蓋</h1><p  class=" wow animate__animated animate__fadeInRight" data-wow-duration="1s" data-wow-delay="0.4s">Coverage/</p></div> </div> 
</div>
<div class="fixed_scroll"> <div class="fixed_scroll_text">Scroll</div> </div>
<div class="clear clear-both"></div>

<div class="about_container about_container_region">

    <div class="part part_left">

<div class="about_region_title"> <h1  class=" wow animate__animated animate__fadeInLeft" data-wow-duration="1s" data-wow-delay="0.2s">香港</h1> <p  class=" wow animate__animated animate__fadeInLeft" data-wow-duration="1s" data-wow-delay="0.2s">/////////////////</p> <p >34間醫療機構</p> <p>HONG KONG</p> </div>
<div class="about_region_boxs">
  <div class="about_region_items">
    <div class="about_region_item"><div class="line_bg"></div><div class="about_region_cricle"> <div class="icon"></div><p>1間腫瘤專科 <br> 中心</p>  </div> </div> 
    <div class="about_region_item"><div class="line_bg"></div><div class="about_region_cricle">  <div class="icon"></div><p>1間家庭醫學 <br>中心</p>  </div> </div> 
    <div class="about_region_item"><div class="line_bg"></div><div class="about_region_cricle">  <div class="icon"></div><p>15間眼科中心和 <br>日間手術中心</p>  </div> </div> 
    <div class="about_region_item"><div class="line_bg"></div><div class="about_region_cricle">  <div class="icon"></div><p>2間微笑矯中心</p>  </div> </div> 
    <div class="about_region_item"><div class="line_bg"></div><div class="about_region_cricle">  <div class="icon"></div><p>1間新冠病毒 <br>檢測中心</p>  </div> </div> 
    <div class="about_region_item"><div class="line_bg"></div><div class="about_region_cricle">  <div class="icon"></div><p>2間醫美中心</p>  </div> </div> 
    <div class="about_region_item"><div class="line_bg"></div><div class="line_bg"></div><div class="about_region_cricle">  <div class="icon"></div><p>7間牙科中心</p>  </div> </div> 
    <div class="about_region_item"><div class="line_bg"></div><div class="about_region_cricle">  <div class="icon"></div><p>5間視光中心</p>  </div> </div> 
  </div>
</div>

    </div>

    <div class="part part_right">

<div class="about_region_boxs flex justify-end">
  <div class="about_region_items">
    <div class="about_region_item"><div class="line_bg"></div><div class="about_region_cricle"> <div class="icon"></div><p>1間腫瘤專科 <br> 中心</p>  </div> </div> 
    <div class="about_region_item"><div class="line_bg"></div><div class="about_region_cricle">  <div class="icon"></div><p>1間家庭醫學 <br>中心</p>  </div> </div> 
    <div class="about_region_item"><div class="line_bg"></div><div class="about_region_cricle">  <div class="icon"></div><p>15間眼科中心和 <br>日間手術中心</p>  </div> </div> 
    <div class="about_region_item"><div class="line_bg"></div><div class="about_region_cricle">  <div class="icon"></div><p>2間微笑矯中心</p>  </div> </div> 
    <div class="about_region_item"><div class="line_bg"></div><div class="about_region_cricle">  <div class="icon"></div><p>1間新冠病毒 <br>檢測中心</p>  </div> </div> 
    <div class="about_region_item"><div class="line_bg"></div><div class="about_region_cricle">  <div class="icon"></div><p>2間醫美中心</p>  </div> </div> 
  </div>
</div>
<div class="about_region_title"> <h1>內地</h1> <p>/////////////////</p>  <p></p> <p>MAINLAND</p> </div>
    </div>

    
</div>
<Footer />
</div>
</template>
<style scoped>
/* animate */
@-webkit-keyframes fadeBg { 0% { width: 100%; } to { width: 0%; } }
@keyframes fadeBg { 0% { width: 100%; } to { width: 0%; } }
.animate__fadeBg { -webkit-animation-name: fadeBg; animation-name: fadeBg }
/* animate end */


.about_container_region{overflow-x: hidden;}
.about_container_region .part{display: flex;justify-content: space-between;align-items: flex-start;}
.about_container_region .part.part_right{align-items: flex-end;position: relative;}
.about_container_region .part.part_left .about_region_title{width: 40%;transform: translateX(7vw);}
.about_container_region .part.part_right .about_region_title{width: 40%;}
.about_container_region .part.part_left .about_region_boxs{width: 60%;background-image: url(@/assets/images/about/HKMap.jpg); background-size: 74%;   background-repeat: no-repeat; background-position: right top;}
.about_container_region .part.part_right .about_region_boxs{width: 60%;background-image: url(@/assets/images/about/ChinaMap.jpg); background-size: 80%;   background-repeat: no-repeat; background-position: left 4vw top;}
.about_container_region .about_region_boxs .about_region_items{width: 34.4vw;height: 34.4vw;position: relative;}
 
.about_container_region .about_region_item{width: 8.6vw;height: 8.6vw; }
.about_container_region .about_region_item .about_region_cricle{background-color: #FFFFFF;border-radius: 50%;border: 1px solid #F09038; box-sizing: border-box;text-align: center;z-index: 2; position: relative;width: 100%;height: 100%;display: flex;justify-content: center;align-items: center;flex-flow: column;z-index: 1;overflow: hidden;transition: all .3s ease-out;}
.about_container_region .about_region_item:hover .about_region_cricle{background: #F09038;transform: scale(1.1);box-shadow: 5px 5px 10px lightgray;border-color:#FFFFFF ;}
.about_container_region .about_region_item .about_region_cricle::before{ content: ''; z-index: 3; position: absolute;width: 10vw;height: 3vw;border-radius: 100%; background:linear-gradient(177.65deg, rgba(255, 255, 255, 0) -34.65%, #FFFFFF 8.91%, #FFFFFF 24.26%, rgba(240, 144, 56, 0) 59.79%);;transform: rotate(-45deg);bottom: -2.5vw;right: -6vw;transition: all .5s ease-out;}
.about_container_region .about_region_item:hover .about_region_cricle::before{transform:translate(-8vw,-8vw) rotate(-45deg);height: 2vw;}
.about_container_region .about_region_item p{font-size: .8vw;}
.about_container_region .about_region_item:hover  p{color: #FFFFFF;}
.about_container_region .about_region_item .icon{width: 2vw;height: 3vw;}



.about_container_region .about_region_item:nth-child(1) .icon{background: url(@/assets/images/about/Group 71.svg) no-repeat center;background-size: 100% auto;}
.about_container_region .about_region_item:nth-child(2) .icon{background: url(@/assets/images/about/Group 73.svg) no-repeat center;background-size: 100% auto;}
.about_container_region .about_region_item:nth-child(3) .icon{background: url(@/assets/images/about/Group 78.svg) no-repeat center;background-size: 100% auto;}
.about_container_region .about_region_item:nth-child(4) .icon{background: url(@/assets/images/about/Group 76.svg) no-repeat center;background-size: 100% auto;}
.about_container_region .about_region_item:nth-child(5) .icon{background: url(@/assets/images/about/Group 84.svg) no-repeat center;background-size: 100% auto;}
.about_container_region .about_region_item:nth-child(6) .icon{background: url(@/assets/images/about/Group 70.svg) no-repeat center;background-size: 100% auto;}
.about_container_region .about_region_item:nth-child(7) .icon{background: url(@/assets/images/about/Group 79.svg) no-repeat center;background-size: 100% auto;}
.about_container_region .about_region_item:nth-child(8) .icon{background: url(@/assets/images/about/Group 86.svg) no-repeat center;background-size: 100% auto;}

.about_container_region .about_region_item:nth-child(1):hover .icon{background: url(@/assets/images/about/region/Group 71.svg) no-repeat center;background-size: 100% auto;}
.about_container_region .about_region_item:nth-child(2):hover .icon{background: url(@/assets/images/about/region/Group 73.svg) no-repeat center;background-size: 100% auto;}
.about_container_region .about_region_item:nth-child(3):hover .icon{background: url(@/assets/images/about/region/Group 78.svg) no-repeat center;background-size: 100% auto;}
.about_container_region .about_region_item:nth-child(4):hover .icon{background: url(@/assets/images/about/region/Group 76.svg) no-repeat center;background-size: 100% auto;}
.about_container_region .about_region_item:nth-child(5):hover .icon{background: url(@/assets/images/about/region/Group 84.svg) no-repeat center;background-size: 100% auto;}
.about_container_region .about_region_item:nth-child(6):hover .icon{background: url(@/assets/images/about/region/Group 70.svg) no-repeat center;background-size: 100% auto;}
.about_container_region .about_region_item:nth-child(7):hover .icon{background: url(@/assets/images/about/region/Group 79.svg) no-repeat center;background-size: 100% auto;}
.about_container_region .about_region_item:nth-child(8):hover .icon{background: url(@/assets/images/about/region/Group 86.svg) no-repeat center;background-size: 100% auto;}

.about_container_region .about_region_item .line_bg{position: absolute; content: ''; width: 8vw; height: 1px; background: #F09038;z-index: 0;}
.about_container_region .about_region_item:nth-child(1) .line_bg{top: 0vw; left: 4vw; transform: rotate(-45deg);}
.about_container_region .about_region_item:nth-child(2) .line_bg{top: 0;bottom: 0;margin: auto; right: -4vw;  }
.about_container_region .about_region_item:nth-child(3) .line_bg {display: none;}
.about_container_region .about_region_item:nth-child(4) .line_bg{top: 0vw; right: 4vw; transform: rotate(45deg);}
.about_container_region .about_region_item:nth-child(5) .line_bg{top: 0vw;left: 0;right: 0;margin: auto;  transform: rotate(90deg);}
.about_container_region .about_region_item:nth-child(6) .line_bg{top: 0vw; left: -4vw; transform: rotate(45deg);}
.about_container_region .about_region_item:nth-child(7) .line_bg:nth-child(1){top: 0vw;bottom: 0;margin: auto; left: -4vw;}
.about_container_region .about_region_item:nth-child(7) .line_bg:nth-child(2){bottom: 8.5vw;right: -4vw; transform: rotate(-45deg);}
.about_container_region .about_region_item:nth-child(8) .line_bg{top: 0vw;left: 0;right: 0;margin: auto;  transform: rotate(90deg);}

.about_container_region .part_right .about_region_item:nth-child(1) .line_bg{top: 0vw; left: 3vw; transform: rotate(-55deg);}
.about_container_region .part_right .about_region_item:nth-child(2) .line_bg{top: 0;bottom: 0;margin: auto; right: -4vw;  }
.about_container_region .part_right .about_region_item:nth-child(3) .line_bg {display:block; transform: rotate(55deg);bottom: 0vw; right: -4vw; }
.about_container_region .part_right .about_region_item:nth-child(4) .line_bg{bottom: 0vw; top: unset;left: unset;margin: unset; right: 3vw; transform: rotate(-55deg);}
.about_container_region .part_right .about_region_item:nth-child(5) .line_bg{top: 0vw;left: -3vw;right: unset;transform: rotate(55deg);}
.about_container_region .part_right .about_region_item:nth-child(6) .line_bg{top: 0;bottom: 0;margin: auto; left: -3vw; transform: rotate(0);}

.about_container_region .about_region_item:nth-child(1){position: absolute;top: 7.5vw;}
.about_container_region .about_region_item:nth-child(2){position: absolute;top: 0vw;left: 7.5vw;}
.about_container_region .about_region_item:nth-child(3){position: absolute;top: 0vw;right: 7.5vw;}
.about_container_region .about_region_item:nth-child(4){position: absolute;top: 7.5vw;right: 0;}
.about_container_region .about_region_item:nth-child(5){position: absolute;bottom: 7.5vw;left: 0;}
.about_container_region .about_region_item:nth-child(6){position: absolute;bottom: 0;left: 7.5vw;}
.about_container_region .about_region_item:nth-child(7){position: absolute;bottom: 0;right: 7.5vw;}
.about_container_region .about_region_item:nth-child(8){position: absolute;bottom: 7.5vw;right: 0;}

.about_container_region .part_right .about_region_item:nth-child(1){position: absolute;top: 10vw;}
.about_container_region .part_right .about_region_item:nth-child(2){position: absolute;top: 0vw;left: 7.5vw;}
.about_container_region .part_right .about_region_item:nth-child(3){position: absolute;top: 0vw;right: 7.5vw;}
.about_container_region .part_right .about_region_item:nth-child(4){position: absolute;top: 10vw;right: 0;}
.about_container_region .part_right .about_region_item:nth-child(5){position: absolute;bottom: 6vw;left: 7.5vw;}
.about_container_region .part_right .about_region_item:nth-child(6){position: absolute;bottom: 6vw;right: 7.5vw;left: unset;}

.part{margin: 100px 0;}
.about_container{max-width:80vw;margin: auto;}
.about_container p{font-size: 20px;font-weight: 300;}

.about_region_title h1{font-weight: 300; font-size: 3vw;line-height: 5.4vw;  letter-spacing: 0.1em; color: #80C5DE;position: relative;z-index: 5;}
.about_region_title p:nth-child(2){font-family: 'Metropolis'; font-style: normal; font-weight: 100; font-size: 3vw; line-height: 2vw; /* identical to box height */ letter-spacing: 0.25em; color: #F09038;position: relative;z-index: 4;transform: translate(1.2vw,-1.5vw) ;}
.part_right .about_region_title h1{text-align: right;transform: translate(-12vw,-8.5vw);font-weight: 300;}

.about_region_title p:nth-child(3){font-family: 'Noto Sans HK'; font-style: normal; font-weight: 400; font-size: 1.95vw; line-height: 3vw; /* identical to box height, or 141% */ letter-spacing: 0.1em; color: #80C5DE;transform: translate(10.6vw, -1vw);position: relative;z-index: 5;}
.about_region_title p:nth-child(4){font-family: 'Metropolis'; font-style: normal; font-weight: 400; font-size: 3.7vw; line-height: 8vw; /* identical to box height, or 214% */ letter-spacing: 0.05em; color: #F3F3F3;transform: translate(-7.3vw, -2vw);}
.part_right .about_region_title p:nth-child(2){transform: translate(-3.8vw, -10.5vw);}
.part_right .about_region_title p:nth-child(4){position: absolute;content: '';top: 0;bottom: 0;margin: auto;display: flex; align-items: center;transform: translate(10.7vw, -3vw);}

.fixed_scroll{left: unset;right: 1vw;}

.banner_region_box{position: relative;}
.banner_region_animatebg{position: absolute;right: 0; content: '';width: 100%;height: 100%;background: #FFFFFF;z-index: 9;}
.banner_region{height: calc(100vh - 141px);position: relative;}
.banner_region_bgpic{position: absolute;left: 0; width: 83.5vw;height: 100%;background-image: url(@/assets/images/about/about_region.jpg);background-repeat: no-repeat;background-position: left center;background-size:   100%;}
.banner_region .banner_about_text{position: absolute; top: 8vw;  right: 10.5vw; display: flex; flex-flow: column; align-items: flex-start; justify-content: center; z-index: 2;}
.banner_region .banner_about_text h1 { font-weight: 400; font-size: 3vw; letter-spacing: 0.2em; color: #80C5DE; }
.banner_region .banner_about_text p { font-weight: 400; font-size: 2.1vw; letter-spacing: 0.2em; color: #FFFFFF; font-family: 'Metropolis';margin-left: -6vw; }


@media screen and   (max-width: 1500px) {
.about_page .part_one_box{max-width: 100%;}      
.about_page .part_one_box .txt{max-width: unset;width: 50vw;}
.about_page .part_one::after{right: 1vw;}      
}
@media screen and   (min-width: 1500px) {
.about_page .part_two_box_pic:nth-child(3) img:nth-child(2){margin-left: -3vw;}
      
}
</style>

<script>
import Menu from "@/components/commom/head/Menu.vue"
import Footer from "@/components/commom/foot/Footer.vue"

export default {
 components: { Menu, Footer },
}
</script>