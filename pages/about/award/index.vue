<template>
      <div class="">
<Menu />
<div class="banner_award_box">
<div class="banner_award_bgcolor"></div>
<div class="banner_award"> <div class="banner_about_text"><h1>獎項及嘉許</h1><p>Rewards/</p></div> </div> 
</div>
<div class="fixed_scroll"> <div class="fixed_scroll_text">Scroll</div> </div>
<div class="clear clear-both"></div>

<div class="about_container">
    <div class="part">
        <div class="titile text-center">
            <div class="icon mb-4"><img class="inline" src="@/assets/images/about/about_award_icon1.svg" alt="" srcset=""></div>
            <h1>雄厚 <img class="inline" src="@/assets/images/about/cmer.svg" alt="" srcset=""> 實力</h1>
        </div>

        <table>
            <tr>
                <th>年份</th>
                <th>獎項</th>
                <th>主辦機構</th>
            </tr>
        </table>
    </div>
</div>


 

<Footer />

</div>
</template>

<style scoped>
.part{margin: 100px 0;}
.about_container{max-width:1200px;margin: auto;}
.about_container p{font-size: 20px;font-weight: 300;}

.titile h1{font-size: 37.0321px; line-height: 54px; /* identical to box height */ letter-spacing: 0.1em; color: #80C5DE; }

.banner_award_box{position: relative;}
.banner_award_bgcolor{background-color: #80C5DE;width: 30vw;height: 26vw;position: absolute;top: 6vw;}
.banner_award{height: calc(100vh - 141px);background-image: url(@/assets/images/about/about_award.jpg);background-repeat: no-repeat;background-position: right;background-size: auto 100%;position: relative;}
.banner_award .banner_about_text{position: absolute; top: 9vw;  left: 10%; display: flex; flex-flow: column; align-items: flex-start; justify-content: center; z-index: 2;}
.banner_award .banner_about_text h1 { font-weight: 400; font-size: 3vw; letter-spacing: 0.2em; color: #404040; }
.banner_award .banner_about_text p { font-weight: 400; font-size: 2.1vw; letter-spacing: 0.2em; color: #FFFFFF; font-family: 'Metropolis'; }


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