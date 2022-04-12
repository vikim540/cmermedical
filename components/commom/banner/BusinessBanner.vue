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
.businessBanner {
  position: relative;
}
.bannerimg img {
  width: 82vw;
}

.bannertext {
  position: absolute;
  right: 13vw;
  top: 6vw;
}

.bannertext h1 {
  background: rgba(255, 255, 255, 0.7);
  font-size: 2.5vw;
  margin-bottom: 2vw;
  display: inline-block;
  padding: 2vw 3vw;
  padding-right: 0;
}

.bannertext .maintext {
  background: rgba(255, 255, 255, 0.7);
  width: 23vw;
  text-indent: 2.2vw;
  padding: 2vw 3vw;
  padding-right: 0;
  text-align: justify;
}
</style>