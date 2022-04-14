<template>
      <div class="">
<Menu />
<div class="banner_about float-right w-3/4">
    <img class="inline w-full" src="@/assets/images/about/about_introduction.jpg" alt=""> 
    <div class="banner_about_test"><h1>集團介紹</h1><p>About Us/</p></div>           
    <div class="pic"><img class="w-full" src="@/assets/images/about/about_introduction_p1left.jpg" alt="" srcset="">  </div>
    </div> 
<div class="fixed_scroll"> <div class="fixed_scroll_text">Scroll</div> </div>
<div class="clear clear-both"></div>

 <div class="about_page">

<div class="part part_one part_bg_fang">
    <div class="part_one_box ">
          
          <div class="txt">希瑪眼科醫療控股有限公司 (「希瑪醫療」或「本集團」) (股份代號：3309) 是香港領先的醫療集團之一，總部設於香港，提供多元化的專科醫療服務，範圍涵蓋眼科、腸胃科、腫瘤科、牙科、體檢中心、家庭醫學及整型外科／醫學美容等。本集團的綜合專科醫療由一支臨床經驗豐富的專科醫生團隊提供，致力為客戶提供專業優質和價格合理的一站式專科醫療服務。</div>
    </div>
</div>  

<div class="part part_two">
<div class="about_container">
<div class="part_two_box part_bg_fang">

<div class="part_two_box_txt"> <p>希瑪醫療現時於香港擁有超過30家醫療機構，地點遍佈各主要地區，交通便利。各醫療中心均配備先進完善的醫療設備，環境佈置舒適，讓客戶獲得安心貼心、專業可靠的服務體驗。</p><p>  作為由醫生創辦和經營管理的上市醫療集團，希瑪醫療秉持嚴謹的專業操守。本集團僱用超過1,400名員工，專業醫護團隊憑藉其豐富經驗和獨特專長，採用與國際接軌的科技和治療方式，專注為客戶度身設計最合適的治療方案。醫療服務包括專科診症、針對性的專科檢查、藥物治療、日間門診手術和跟進治療等。如有需要，中心亦可為病人安排入院進行手術治療。</p> </div>

<div class="part_two_box_pic translate-y-20">
      <img class="w-full" src="@/assets/images/about/about_introduction_p2left.jpg" alt="" sizes="" srcset="">
</div>

<div class="part_two_box_pic">
      <img class="w-full" src="@/assets/images/about/about_introduction_p2r1.jpg" alt="" sizes="" srcset="">
      <img class="w-full" src="@/assets/images/about/about_introduction_p2r2.jpg" alt="" sizes="" srcset="">
</div> </div> </div> </div> 

<div class="part part_three">
      <div class="part_three_pic"><img class="w-full" src="@/assets/images/about/about_introduction_p3.jpg" alt="" sizes="" srcset=""></div>
      <div class="about_container">
 <p>除了香港業務外，希瑪醫療在內地建立一個以大灣區為主的全國性實體醫院網路，共設有28間眼科和牙科醫院和門診部，遍及包括深圳和廣州等大灣區多個城市、北京、上海、昆明和福州等地，方便內地居民就近獲得希瑪的優質港式醫療服務。 </p><p>為滿足市民對優質專科醫療的需求，本集團未來將繼續擴展至更多專科服務，在不同地區開設更多醫療中心，並且持續提升醫療技術水平，追求服務卓越，讓希瑪醫療成為香港市民的專科醫療信心品牌。</p>
 <p class="slash"> <span style="color:#F09038;">/////////</span>  <span style="color:#80C5DE;">////////</span> </p>
      </div>
</div>


</div>

<Footer />

</div>
</template>

<style scoped>
.part{margin: 100px 0;}
.about_container{max-width:68vw;margin: auto;}
.about_container p{font-size: 20px;font-weight: 300;}



/* -------------------------------------- */
.about_page .part_one,.about_page .part_bg_fang{position: relative;}
.about_page .part_bg_fang::before{position: absolute;content: '';width:20px;height: 20px;top: 3vw;right: 11vw;z-index: -1;border-top:2px solid #F09038;border-right: 2px solid #F09038;}
.about_page .part_two .part_bg_fang::before{right: unset !important;left: -50px;top: -50px;border-left: 2px solid #F09038;border-top: 2px solid #F09038;border-right: none;border-bottom: none;}

/* -------------------------------------- */
.about_page .part_one{z-index: -1;}
.about_page .part_one::after{position: absolute;content: '/////////////////';width:27vw;bottom: 0.5vw;right: 11vw;z-index: -1;color: #F09038;font-size: 2.5vw; letter-spacing: 0.25em;font-family: 'Metropolis';text-align: right;z-index: 9;font-weight: 100;}
.about_page .part_one_box{background: #80C5DE;padding: 4vw 6vw;padding-left: 32vw; max-width: 70%;display: flex;align-items: center;justify-content: space-between;}
.about_page .part_one_box .pic{width: 26vw;max-width: 500px;} 
.about_page .part_one_box>div{display: inline-block;}
.about_page .part_one_box .pic{float: left;position: relative;z-index: 0;margin-top: -39vw;}
.about_page .part_one_box .txt{width: 30vw;margin-left: 30px;font-size: 20px; line-height: 40px; /* or 200% */ text-align: justify; letter-spacing: 0.15em; text-indent: 50px; color: #FFFFFF;font-weight: 300;}
/* -------------------------------------- */
.about_page .part_two .part_two_box{display: flex;justify-content: space-between;padding-bottom: 100px;}
.about_page .part_two .part_two_box_txt{width: 21.6vw;padding-right: 1vw; font-size: 20px; line-height: 40px; /* or 200% */ text-align: justify; letter-spacing: 0.15em; text-indent: 50px; color: #404040;}
.about_page .part_two .part_two_box_txt p:first-child{margin-bottom: 40px;}
.about_page .part_two_box_pic:nth-child(2){max-width: 18.1vw;margin-left: -5vw;}
.about_page .part_two_box_pic:nth-child(3){max-width: 20vw;}
.about_page .part_two_box_pic:nth-child(3) img:nth-child(1){transform: translateY(-2vw);}
.about_page .part_two_box_pic:nth-child(3) img:nth-child(2){transform: translateX(-1vw);margin-left: -6.1vw;}
/* -------------------------------------- */
.about_page .part_three{position: relative;background: #F3F3F3;margin-bottom: 100px;}
.about_page .part_three::before{position: absolute;content: ''; left: 0;top: 0;width: 15.6vw;height: 100%;background: #FFFFFF;}
.about_page .part_three .part_three_pic{position: absolute;width: 43vw;top: 200px;left: 0;}
.about_page .part_three .about_container{background: #F3F3F3;padding-top: 60px;padding-bottom: 100px;padding-left:30vw;}
.about_page .part_three .about_container p{font-size: 20px; line-height: 40px; /* or 200% */ text-align: justify; letter-spacing: 0.15em; text-indent: 50px; color: #404040;}
.about_page .part_three .about_container p:first-child{margin-bottom: 40px;}
.about_page .part_three .slash{position: absolute; bottom: -1.3vw; color: #F09038;left: 0;right: 0;margin: auto;text-align: center !important; }
.about_page .part_three .slash span{font-size: 3vw; letter-spacing: 0.3vw;  }


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