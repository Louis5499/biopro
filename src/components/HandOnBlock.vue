<template>
  <div class="hand-wrapper">
    <div class="header">
      <img src="@/assets/icon_speaker.svg" width="30px"/>
      <h2 class="title">Hand-ons Project</h2>
    </div>
    <div class="content">
      <div class="speaker-block" v-for="(speaker, idx) in speakers" :key="idx">
        <h3 class="speaker-name">{{speaker.name}}</h3>
        <p class="speaker-brief">{{speaker.brief}}</p>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      modalShow: 0,
      speakers: [
        {
          name: `Reading Attributes from Hands`,
          brief: `Prof. Hwann-Tzong Chen`,
        },
        {
          name: `Intelligence tactile sensing system implementation`,
          brief: `Prof. Nitish Thakor`,
        },
        {
          name: `Real-time action potential detection`,
          brief: `Prof. Yannick Bornat`,
        },
        {
          name: `Event driven tactile sensing`,
          brief: `Prof. Chiara Bartolozzi`,
        }
      ]
    }
  },
  watch: {
    agendaChooseNum() {
      this.modalShow = this.agendaChooseNum;
    }
  }
}
</script>

<style lang="scss" scoped>
.hand-wrapper {
  width: 100vw;
  display: flex;
  flex-direction: column;
  align-items: center;
  .header {
    display: flex;
    flex-direction: row;
    align-items: center;
    img {
      margin-right: 20px;
    }
    h2 {
      font-size: 2em;
      letter-spacing: 5px;
      color: rgb(54, 93, 150);
    }
  }
  .content {
    display: flex;
    justify-content: center;
    width: 100vw;
    flex-wrap: wrap;
    .speaker-block {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      max-width: 680px;
      width: 80%;
      box-shadow: 0px 1px 10px rgba(#666,.3);
      margin: 30px 30px;
      .speaker-avatar {
        width: 150px;
        height: 150px;
        border-radius: 50%;
        object-fit: cover;
      }
      .speaker-content {
        margin-left: 30px;
        display: flex;
        flex-direction: column;
        width: 60%;
        padding: 30px 0;
        .speaker-name {
          font-size: 2em;
          color: #757575;
          margin: 0;
        }
        .speaker-brief {
        }
        .speaker-link {
          display: flex;
          flex-direction: row;
          align-items: center;
          color: #666;
          img {
            margin-right: 10px;
          }
        }
        .more-button {
          margin-top: 20px;
          padding: 8px 15px;
          border: #666 1px solid;
          width: fit-content;
          cursor: pointer;
          transition: .1s all linear;
          &:hover {
            background-color: #666;
            color: white;
          }
        }
      }
    }
  }
}
@media all and (min-width: 1220px) {
  .hand-wrapper {
    .header {
      font-size: 1.2em;
    }
  }
}
@media all and (max-width: 630px) {
  .speaker-block {
    flex-direction: column !important;
    .speaker-avatar {
      margin: 20px 0 0 0;
    }
    .speaker-content {
      margin: 0 !important;
      width: 80% !important;
    }
  }
}
</style>

