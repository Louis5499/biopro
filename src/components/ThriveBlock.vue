<template>
  <el-row class="row-wrapper" :gutter="20" type="flex" align="middle">
    <el-col :span="10">
      <div class="text-header">
        <img src="@/assets/icon_people.svg" />
        <h2>Thrive & Prosper</h2>
      </div>
      <div class="text-content">
        <p>In 2017, the BioPro A+ Platform has funded more students to work with world-leading experts in bio-inspired systems, bio-electronics and machine intelligence.</p>
        <p>In this exciting event, we would like to share our experience and joy with you, as well as to provide the opportunity for you to interact with international researchers and students in related fields.</p>
      </div>
    </el-col>
    <el-col :span="14">
      <el-carousel :interval="4000" type="card" height="300px">
        <el-carousel-item><img height="100%" src="@/assets/img_1.png"/></el-carousel-item>
        <el-carousel-item><img height="100%" src="@/assets/img_2.png"/></el-carousel-item>
        <el-carousel-item><img height="100%" src="@/assets/img_3.png"/></el-carousel-item>
        <el-carousel-item><img height="100%" src="@/assets/img_4.png"/></el-carousel-item>
      </el-carousel>
    </el-col>
  </el-row>
</template>

<script>
export default {
  
}
</script>

<style lang="scss" scoped>
.row-wrapper {
  padding: 0 10%;
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
  }
}
@media all and (min-width: 1220px) {
  .row-wrapper {
    font-size: 1.2em;
  }
}
</style>

