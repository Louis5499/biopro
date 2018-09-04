<template>
  <div class="head-wrapper">
    <img class="background" src="@/assets/top_banner_bg.svg">
    <div class="nav">
      <div class="logo">Biopro A+</div>
      <div class="option-wrapper">
        <div class="nav-option">Program</div>
        <div class="nav-option">Speakers</div>
        <div class="nav-option">Call for Posters</div>
        <div class="nav-option">Location</div>
        <div class="nav-option register">Register</div>
      </div>
    </div>
    <div class="text-block">
      <div class="upper-text">
        <span>Beyond A+</span>
        <span>2019 International Workshop</span>
      </div>
      <div class="below-text">
        <span>Bio-inspired Systems</span>
        <div class="line"></div>
        <span>Machine Intelligence</span>
        <div class="line"></div>
        <span>Bio-electronics</span>
      </div>
      <div class="btn-register">Register</div>
    </div>
    <div class="map-block">
      <iframe width="100%" height="70%" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="https://www.openstreetmap.org/export/embed.html?bbox=120.98391294479372%2C24.78800079239005%2C121.00537061691284%2C24.802571482206947&amp;layer=mapnik&amp;marker=24.795282774950017%2C120.99464672617614"></iframe>
      <div class="below-block">
        <img class="arrow" src="@/assets/right_arrow.svg"/>
        <div class="inner-text-block">
          <span>26 - 28 Jan</span>
          <span>NTHU</span>
        </div>
      </div>
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
.head-wrapper {
  display: flex;
  flex-direction: column;
  width: 100vw;
  height: 50vw;
  position: relative;
  align-items: center;
  .background {
    position: absolute;
    width: 100%;
    z-index: 0;
  }
  .nav {
    z-index: 1;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 88%;
    color: white;
    margin-top: 30px;
    .logo {
      font-size: 2em;
    }
    .option-wrapper {
      display: flex;
      flex-direction: row;
      .nav-option {
        margin: 0 10px;
        cursor: pointer;
        height: 30px;
        padding: 0 20px;
        display: flex;
        align-items: center;
        justify-content: center;
        &.register {
          border: 1px solid white;
          border-radius: 5px;
        }
      }
    }
  }
  .text-block {
    z-index: 1;
    width: 54%;
    display: flex;
    flex-direction: column;
    color: white;
    font-size: 1.5em;
    position: absolute;
    left: 6%;
    top: 40%;
    .upper-text {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      font-size: 1.2em;
      margin-bottom: 10px;
    }
    .below-text {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      font-size: .8em;
      margin-bottom: 20px;
      .line {
        width: 1px;
        height: 15px;
        background: rgb(107, 151, 255);
        margin: 0 20px;
      }
    }
    .btn-register {
      width: 110px;
      height: 40px;
      background-color: #fff;
      border-radius: 10px;
      color: rgb(0, 151, 255);
      font-size: .8em;

      display: flex;
      align-items: center;
      justify-content: center;
    }
  }
  .map-block {
    z-index: 1;
    width: 20vw;
    height: 27vw;
    background: white;
    border-radius: 5px;
    box-shadow: 1px 1px rgba(#1c1c1c, .5);

    position: absolute;
    right: 10%;
    top: 30%;
    overflow: hidden;
    .below-block {
      width: 100%;
      height: 30%;
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
      img {
        height: 30%;
        margin-right: 40px;
      }
      .inner-text-block {
        color: #7c7c7c;
        display: flex;
        flex-direction: column;
        font-size: 2.2em;
        letter-spacing: 2px;
        span:nth-child(1) {
          font-size: .7em;
        }
      }
    }
  }
}
</style>
