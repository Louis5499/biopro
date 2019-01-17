<template>
  <div class="poster-wrapper">
    <div class="poster-img" :style="pictureBgCss('../static/img_1.png')"></div>
    <div class="poster-word-block">
      <div class="word-header">Participation</div>
      <div class="word-description">
        <div class="white-line"></div>
        <div class="des-wrapper">
          <p class="description-text"> Totally Free for All Activities! (Max. 100 persons)</p>
          <p class="smaller">A deposit of 350 NTD is required for your registration. The deposit will be fully refunded by the end of the fourth day.</p>
        </div>
      </div>
      <div class="word-text">
        <p>2019 3/14 - 3/17</p>
        <p>NTHU, HsinChu City, Taiwan</p>
        <div class="btn-register" @click="changeRoute()">Register</div>
        <p class="smaller" style="marginTop: 30px">For participants who need accomodation, you can book accomodation in our registration page for 500 NTD/night/person.</p>
        <p class="smaller">Registration deadline ends on 2/12.</p>
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
      height: 70px;
      margin-bottom: 30px;
      .white-line {
        height: 100%;
        width: 10px;
        background-color: #fff;
      }
      .des-wrapper {
        display: flex;
        flex-direction: column;
        margin-left: 10px;
        .description-text {
          font-size: 1.2em;
          margin: 10px 0;
        }
        .smaller {
          font-size: .6em;
          margin: 0;
          line-height: 20px;
        }
      }
    }
    .word-text {
      margin-top: 50px;
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
