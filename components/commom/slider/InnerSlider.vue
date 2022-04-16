<template>
  <div class="section md:font-black">
    <!--  -->
    <div class="inner_slider">
      <div v-swiper:mySwiper="swiperOption" class="swiperWrap ">
        <div class="swiper-wrapper">
          <div class="swiper-slide" v-for="(banner,index) in banners" :key="index">
            <img :src="banner">
          </div>
        </div>
        <!-- <div class="swiper-pagination swiper-pagination-bullets"></div> -->
        <div class=" bg-white flex items-center justify-center bt_box">
          <div class="swiper-button-prev "> <i class="fa fa-angle-left" aria-hidden="true" style="color:#F09038;"></i> </div>
          <div class="swiper-pagination"></div>
          <div class="swiper-button-next"><i class="fa fa-angle-right" aria-hidden="true" style="color:#F09038;"></i> </div>
        </div>

      </div>

    </div>

  </div>
</template>
<script>
export default {
  data() {
    return {
      banners: [
        require('../../../assets/images/business/cmereye/eyecenter1.jpg'),
        require('../../../assets/images/business/cmereye/eyecenter1.jpg'),
        require('../../../assets/images/business/cmereye/eyecenter1.jpg'),
        require('../../../assets/images/business/cmereye/eyecenter1.jpg'),
        require('../../../assets/images/business/cmereye/eyecenter1.jpg'),
      ],
      swiperOption: {
        loop: true,
        centeredSlides: true,
        spaceBetween: 50,
        slidesPerView: "1",
        pagination: {
          el: '.swiper-pagination',
          type: 'fraction',
        },


        navigation: {
          nextEl: ".swiper-button-next", //下一页dom节点
          prevEl: ".swiper-button-prev", //前一页dom节点
        },
        on: {
          slideChange() {
            console.log('onSlideChangeEnd', this);
          },
          tap() {
            console.log('onTap', this);
          }
        }
      }
    }
  },
  created() { },
  methods: {}
};
</script>
<style>
.swiper-button-prev,
.swiper-container-rtl .swiper-button-next,
.swiper-button-next,
.swiper-container-rtl .swiper-button-prev {
  background: none;
}
.swiper-pagination,
.swiper-button-prev,
.swiper-button-next {
  position: static;
}
.swiper-button-prev,
.swiper-button-next {
  width: auto;
  height: auto;
  margin: 0;
}
.bt_box {
  position: absolute;
  width: 13vw;
  bottom: 0;
  z-index: 11;
  height: 3.5vw;
  padding: 0 1vw;
}
</style>