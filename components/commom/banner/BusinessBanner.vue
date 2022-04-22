<template>
  <div class="businessBanner md:flex">
    <div class="bannerimg">
      <img src="../../../assets/images/business/cmereye/bannerimg.jpg" alt="">
    </div>
    <div class="bannertext md:flex  md:items-end md:flex-col">
      <h1 class=" font-black">希瑪眼科</h1>
      <p class="maintext">眼疾是香港常見的疾病之一。隨著人口邁向高齡化，香港65歲及以上長者人口將由2019年的132萬，倍增至2050年的270萬＃，增加各種與老齡化相關的眼科疾病的患病率。與此同時，香港更是全球近視患病率最高的城市之一，估計有四成以上八歲學童患有近視＊。</p>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  created() { },
  methods: {}
};
</script>
<style scoped>
/* common */

.businessBanner {
  position: relative;
}

.bannertext {
  position: absolute;
}

.bannertext h1 {
  background: rgba(255, 255, 255, 0.7);
  display: inline-block;
  padding-right: 0;
}

.bannertext .maintext {
  background: rgba(255, 255, 255, 0.7);
  padding-right: 0;
  text-align: justify;
}
/* pc */
@media only screen and (min-width: 768px) {
  .bannerimg img {
    width: 82vw;
  }

  .bannertext {
    right: 13vw;
    top: 6vw;
  }

  .bannertext h1 {
    font-size: 2.5vw;
    margin-bottom: 2vw;
    padding: 2vw 3vw;
  }

  .bannertext .maintext {
    width: 23vw;
    text-indent: 2.2vw;
    padding: 2vw 3vw;
  }
}
/* md */
@media only screen and (max-width: 768px) {
  .bannerimg img {
    width: 80vw;
  }

  .bannertext {
    right: 0vw;
    top: 0vw;
  }

  .bannertext h1 {
    font-size: 2.5vw;
    margin-bottom: 2vw;
    padding: 2vw 3vw;
  }

  .bannertext .maintext {
    width: 50vw;
    text-indent: 2.2vw;
    padding: 2vw 3vw;
    font-size: 12px;
  }
}
</style>