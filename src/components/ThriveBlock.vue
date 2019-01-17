<template>
  <div class="row-wrapper">
    <div class="left-panel">
      <div class="text-header">
        <img src="@/assets/icon_people.svg" />
        <h2>Thrive & Prosper</h2>
      </div>
      <div class="text-content">
        <p>The <a href="https://www.bioproaplus.org/">BioPro A+ platform</a> has been funded by the Ministry of Education in Taiwan since 2016. Its main mission is providing internship scholarships for students to work with world-leading experts on bio-inspired systems, bio-electronics, and machine intelligence.</p>
        <p>In this exciting event, we would like to share our experiences and joy with you, as well as to provide the opportunity for you to interact with international researchers and students in related fields. For students interested in applying for internship scholarships in 2019, this workshop will be the best chance for you to interact with international researchers directly.</p>
      </div>
    </div>
    <div class="right-panel">
      <el-carousel :interval="4000" trigger="click" height="300px">
        <el-carousel-item><div width="100%" class="caro-img" :style="pictureBgCss('../static/img_1.png')"></div></el-carousel-item>
        <el-carousel-item><div width="100%" class="caro-img" :style="pictureBgCss('../static/img_2.png')"></div></el-carousel-item>
        <el-carousel-item><div width="100%" class="caro-img" :style="pictureBgCss('../static/img_3.png')"></div></el-carousel-item>
        <el-carousel-item><div width="100%" class="caro-img" :style="pictureBgCss('../static/img_4.png')"></div></el-carousel-item>
      </el-carousel>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
  methods: {
    pictureBgCss(img) {
      return { 'background-image': 'url(' + img + ')' };
    }
  }
}
</script>

<style lang="scss" scoped>
.row-wrapper {
  padding: 0 8%;
  display: flex;
  flex-direction: row;
  align-items: center;
  .left-panel {
    width: 50%;
  }
  .right-panel {
    width: 50%;
  }
  .text-header {
    display: flex;
    flex-direction: row;
    align-items: center;
    img {
      width: 100px;
      margin-right: 30px;
    }
    h2 {
      font-size: 2em;
      color: rgb(246, 102, 73);
      letter-spacing: 5px;
    }
  }
  .text-content {
    p {
      color: #7e7e7e;
      line-height: 1.5em;
    }
    a:link {
      color: #a2eae2;
    }
    a:visited {
      color: #caabd8;
    }
  }
  .caro-img {
    width: 100%;
    height: 100%;
    background-position: center center;
    background-size: cover;
  }
}
@media all and (min-width: 1220px) {
  .row-wrapper {
    font-size: 1.2em;
  }
}
@media all and (max-width: 1000px) {
  .row-wrapper {
    flex-direction: column;
    .text-header {
      justify-content: center;
    }
    .left-panel {
      width: 100%;
    }
    .right-panel {
      width: 100%;
    }
  }
}
</style>

