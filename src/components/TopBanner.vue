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
        <div class="nav-option">Register</div>
      </div>
    </div>
    <div class="map-block"></div>
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
    justify-content: space-around;
    color: white;
    .logo {
      font-size: 2em;
      margin: 20px;
    }
    .option-wrapper {
      display: flex;
      flex-direction: row;
      .nav-option {
        margin: 0 10px;
      }
    }
  }
  .map-block {
    z-index: 1;
    width: 20%;
    height: 250px;
    background: white;
    border-radius: 5px;
    box-shadow: 1px 1px rgba(#1c1c1c, .5);

    position: absolute;
    right: 10%;
    top: 120px;
  }
}
</style>
