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
          <div v-if="speaker.pdfLink" class="more-button" @click="modalShow = idx+1">More</div>
        </div>
      </div>
    </div>
    <Modal v-if="modalShow !== 0 && speakers[modalShow-1].pdfLink" @displayReset="modalShow = 0">
      <iframe :src="speakers[modalShow-1].pdfLink" style="width: 90%; height: 90%"></iframe>
    </Modal>
  </div>
</template>

<script>
import Modal from './Modal';
import ProfessorOne from './modalComs/ProfessorOne';
import ProfessorTwo from './modalComs/ProfessorTwo';
import ProfessorThree from './modalComs/ProfessorThree';
import ProfessorFour from './modalComs/ProfessorFour';
import ProfessorFive from './modalComs/ProfessorFive';
import pdf from 'vue-pdf'

export default {
  components: { Modal, ProfessorOne, ProfessorTwo, ProfessorThree, ProfessorFour, ProfessorFive, pdf },
  props: {
    agendaChooseNum: {
      type: Number,
      default: 0
    }
  },
  data() {
    return {
      modalShow: 0,
      speakers: [
        {
          avatarUrl: '../static/avatar_nitish.JPG',
          name: `Prof. Nitish V. Thakor`,
          brief: `Department of Electrical and Computer Engineering and Biomedical Engineering at Johns Hopkins University`,
          link: {
            type: 'email',
            content: 'eletnv@nus.edu.sg'
          },
          pdfLink: `../static/pdf_cvs/nitish.pdf`,
          agendaChooseNum: 1
        },
        {
          avatarUrl: '../static/avatar_abdelhamid.jpeg',
          name: `Prof. Abdelhamid BENAZZOUZ`,
          brief: `Department of Neurodegenerative diseases institute, CNRS UMR 5293 at University of Bordeaux`,
          link: {
            type: 'email',
            content: 'Abdelhamid.benazzouz@u-bordeaux.fr'
          },
          pdfLink: `../static/pdf_cvs/abdelhamid.pdf`,
          agendaChooseNum: 2
        },
        {
          avatarUrl: '../static/avatar_carolina.jpg',
          name: `Prof. Carolina Mora Lopez`,
          brief: `Department of Connected Health Solutions at imec`,
          link: {
            type: 'email',
            content: 'moralope@imec.be'
          },
          pdfLink: `../static/pdf_cvs/carolina.pdf`,
          agendaChooseNum: 3
        },
        {
          avatarUrl: '../static/avatar_chiara.jpg',
          name: `Prof. Chiara Bartolozzi`,
          brief: `Department of iCub Facility at Istituto Italiano di Tecnologia`,
          link: {
            type: 'email',
            content: 'chiara.bartolozzi@iit.it'
          },
          pdfLink: `../static/pdf_cvs/chiara.pdf`,
          agendaChooseNum: 4
        },
        {
          avatarUrl: '../static/avatar_dries.jpg',
          name: `Prof. Dries Braeken`,
          brief: `Department of Life Science Technologies at imec`,
          link: {
            type: 'email',
            content: 'Dries.braeken@imec.be'
          },
          pdfLink: `../static/pdf_cvs/dries.pdf`,
          agendaChooseNum: 5
        },
        {
          avatarUrl: '../static/avatar_tetsushi.jpg',
          name: `Prof. Tetsushi Ohki`,
          brief: `Department of Graduate School of Integrated Science and Technology at Shizuoka University`,
          link: {
            type: 'email',
            content: 'ohki@inf.shizuoka.ac.jp'
          },
          pdfLink: `../static/pdf_cvs/tetsushi.pdf`,
          agendaChooseNum: 6
        },
        {
          avatarUrl: '../static/avatar_ito.gif',
          name: `Prof. Koichi Ito`,
          brief: `Department of ECEI in Tohoku University`,
          link: {
            type: 'email',
            content: 'ito@aoki.ecei.tohoku.ac.jp'
          },
          pdfLink: `../static/pdf_cvs/ito.pdf`,
          agendaChooseNum: 7
        },
        {
          avatarUrl: '../static/avatar_yannick.jpg',
          name: `Prof. Yannick Bornat`,
          brief: `Department of Electronic Engineering in University of Bordeaux `,
          link: {
            type: 'email',
            content: 'yannick.bornat@ims-bordeaux.fr'
          },
          pdfLink: `../static/pdf_cvs/yannick.pdf`,
          agendaChooseNum: 8
        },
        {
          avatarUrl: '../static/avatar_chun.jpg',
          name: `Dr. Chun-Hwei Tai`,
          brief: `Department of Neurology in National Taiwan University Hospital`,
          link: {
            type: 'email',
            content: 'chtai1502@ntu.edu.tw'
          },
          pdfLink: `../static/pdf_cvs/chunhwei.pdf`,
          agendaChooseNum: 9
        },
        {
          avatarUrl: '../static/avatar_hsin.jpg',
          name: `Prof. Hsin Chen`,
          brief: `Department of Electrical Engineering in National Tsing Hua University`,
          link: {
            type: 'email',
            content: 'hchen@ee.nthu.edu.tw'
          },
          pdfLink: `../static/pdf_cvs/hsin.pdf`,
          agendaChooseNum: 10
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
    justify-content: center;
    width: 100vw;
    flex-wrap: wrap;
    .speaker-block {
      display: flex;
      flex-direction: row;
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
  .speaker-wrapper {
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

