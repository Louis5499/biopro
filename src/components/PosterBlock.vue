<template>
  <div class="poster-wrapper">
    <div class="poster-img" :style="pictureBgCss('../static/img_1.png')"></div>
    <div class="poster-word-block">
      <div class="word-header">Participation</div>
      <div class="word-description">
        <div class="white-line"></div>
        <p class="description-text"> Totally for Free! </p>
      </div>
      <div class="word-text">
        <p>2019 3/14 - 3/17</p>
        <p>NTHU, HsinChu City, Taiwan</p>
        <div class="btn-register" @click="changeRoute()">Register</div>
        <p class="smaller" style="marginTop: 30px">You only need to pay for margin, which we would refund you by the end of fourth day.</p>
        <p class="smaller">For those who needs accomodation, We provide accomodation for one person 500 NTD/night.</p>
      </div>
    </div>
    <!-- <div class="poster-word-block">
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
    </div> -->
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
    },
    changeRoute() {
      window.location.href = 'https://bioproaplus.kktix.cc/events/workshop-2019';
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
      height: 40px;
      margin-bottom: 30px;
      .white-line {
        height: 100%;
        width: 10px;
        background-color: #fff;
      }
      .description-text {
        margin-left: 10px;
      }
    }
    .word-text {
      .btn-register {
        width: 80px;
        height: 30px;
        background-color: #fff;
        border-radius: 10px;
        color: rgb(0, 151, 255);
        font-size: .7em;

        margin-top: 10px;

        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        transition: all ease .2s;

        &:hover {
          background-color: rgba(#fff, .9);
        }
      }
      p {
        margin: 0;
        line-height: 1.5em;
        font-weight: 300;
        &.smaller {
          font-size: .75em;
        }
      }
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
