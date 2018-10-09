<template>
  <div class="speaker-wrapper">
    <div class="header">
      <img src="@/assets/icon_speaker.svg" width="30px"/>
      <h2 class="title">Speaker</h2>
    </div>
    <div class="content">
      <div class="speaker-block" v-for="(speaker, idx) in speakers" :key="idx">
        <img class="speaker-avatar" :src="speaker.avatarUrl"/>
        <div class="speaker-content">
          <h3 class="speaker-name">{{speaker.name}}</h3>
          <p class="speaker-brief">{{speaker.brief}}</p>
          <div class="speaker-link">
            <img src="@/assets/icon_website.svg" width="20px"/>
            <span class="link-body">{{speaker.link.content}}</span>
          </div>
          <div class="more-button" @click="modalShow = 1">More</div>
        </div>
      </div>
    </div>
    <Modal v-if="modalShow !== 0" @displayReset="modalShow = 0">
      <ProfessorOne v-if="modalShow === 1"/>
    </Modal>
  </div>
</template>

<script>
import Modal from './Modal';
import ProfessorOne from './modalComs/ProfessorOne';

export default {
  components: { Modal, ProfessorOne },
  data() {
    return {
      modalShow: 0,
      speakers: [
        {
          avatarUrl: '../static/avatar_1.jpg',
          name: `Prof. Sheng-Yu Peng`,
          brief: `Department of Electrical Engineering in National Taiwan University of Science and Technology`,
          link: {
            type: 'email',
            content: 'sypeng@mail.ntust.edu.tw'
          }
        },
        {
          avatarUrl: '../static/avatar_1.jpg',
          name: `Prof. Sheng-Yu Peng`,
          brief: `Department of Electrical Engineering in National Taiwan University of Science and Technology`,
          link: {
            type: 'email',
            content: 'sypeng@mail.ntust.edu.tw'
          }
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.speaker-wrapper {
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
    flex-direction: column;
    align-items: center;
    .speaker-block {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
      width: 85%;
      box-shadow: 0px 1px 10px rgba(#666,.3);
      margin: 30px 0;
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
</style>

