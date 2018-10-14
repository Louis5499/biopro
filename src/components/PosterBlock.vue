<template>
  <div class="poster-wrapper">
    <div class="poster-img" :style="pictureBgCss('../static/img_1.png')"></div>
    <div class="poster-word-block">
      <div class="word-header">Call For Poster</div>
      <div class="word-description">
        <div class="white-line"></div>
        <p class="description-text">
          For those who want to show their talents and share their interesting research, this is a perfect stage for you... 
        </p>
      </div>
      <div class="word-text">
        This year, a poster competition is opened to everyone. Please submit the abstract before 12/29. You would get a chance to present your research in front of world experts. You can also win a big prize!
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
.poster-wrapper {
  width: 100vw;
  height: 40vw;
  transform: skewY(-2deg);
  background-color: #365d96;
  display: flex;
  flex-direction: row;

  margin-top: 80px;
  .poster-img {
    width: 50%;
    height: 100%;

    background-size: cover;
    background-position: center;
  }
  .poster-word-block {
    width: 40%;
    color: white;
    transform: skewY(2deg);
    line-height: 1.5em;

    display: flex;
    flex-direction: column;
    justify-content: center;

    padding-left: 5%;
    .word-header {
      font-size: 2em;
      margin-bottom: 30px;
    }
    .word-description {
      display: flex;
      flex-direction: row;
      align-items: center;
      height: 70px;
      margin-bottom: 30px;
      .white-line {
        height: 100%;
        width: 15px;
        background-color: #fff;
      }
      .description-text {
        margin-left: 10px;
      }
    }
    .word-text {
      line-height: 1.5em;
    }
  }
}

@media all and (max-width: 890px) {
  .poster-wrapper {
    font-size: .8em;
  }
}

@media all and (min-width: 1280px) {
  .poster-wrapper {
    font-size: 1.3em;
  }
}
</style>
