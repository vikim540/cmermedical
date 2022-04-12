<template>
  <div class="section vedio_box md:font-black">
    <div class="flex justify-center">
      <h2>個案分享及矯視資訊影片</h2>
    </div>

    <!--  -->

    <div class="vedio_slider">
      <div v-swiper:mySwiper="swiperOption" class="swiperWrap ">
        <div class="swiper-wrapper">
          <div class="swiper-slide" v-for="(banner,index) in banners" :key="index">
            <img :src="banner.src">
            <nuxt-link class="link_des" :to="banner.link">{{banner.des}}</nuxt-link>
          </div>
        </div>
        <!-- <div class="swiper-pagination swiper-pagination-bullets"></div> -->

        <div class="swiper-button-prev flex items-center justify-center"> </div>
        <div class="swiper-button-next flex items-center justify-center"> </div>

      </div>

      <nuxt-link class="link_more" to="">更多影片</nuxt-link>
    </div>

  </div>
</template>
<script>
export default {
  data() {
    return {
      banners: [

      ],
      swiperOption: {
        loop: true,
        centeredSlides: true,
        spaceBetween: 50,
        slidesPerView: "3",
        pagination: {
          el: '.swiper-pagination',
          dynamicBullets: true
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

</style>