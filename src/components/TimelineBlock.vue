<template>
  <div class="timeline-wrapper">
    <div class="header">
      <img src="@/assets/icon_agenda.svg" width="30px" />
      <h2 class="title">Agenda</h2>
    </div>
    <el-button-group class="select-bar desktop">
      <el-button type="primary" @click="currentSelect = 1" :plain="!isSelected(1)">3/14 (Thu)</el-button>
      <el-button type="primary" @click="currentSelect = 2" :plain="!isSelected(2)">3/15 (Fri)</el-button>
      <el-button type="primary" @click="currentSelect = 3" :plain="!isSelected(3)">3/16 (Sat)</el-button>
      <el-button type="primary" @click="currentSelect = 4" :plain="!isSelected(4)">3/17 (Sun)</el-button>
    </el-button-group>
    <el-button-group class="select-bar mobile">
      <el-button type="primary" @click="currentSelect = 1" :plain="!isSelected(1)">3/14 (Thu)</el-button>
      <el-button type="primary" @click="currentSelect = 2" :plain="!isSelected(2)">3/15 (Fri)</el-button>
    </el-button-group>
    <el-button-group class="select-bar mobile">
      <el-button type="primary" @click="currentSelect = 3" :plain="!isSelected(3)">3/16 (Sat)</el-button>
      <el-button type="primary" @click="currentSelect = 4" :plain="!isSelected(4)">3/17 (Sun)</el-button>
    </el-button-group>
    <div class="content">
      <div v-if="currentSelect === dateIdx+1" class="calender" v-for="(calender, dateIdx) in calenders" :key="dateIdx">
        <div class="title row">
          <div class="left-panel"></div>
          <div class="right-panel">
            <span class="calender-title">{{calender.title}}</span>
            <span class="calender-theme">{{calender.theme}}</span>
          </div>
        </div>
        <div class="body row" v-for="(row, idx) in calender.body" :key="idx" :class="{ thinner: (row.tag === 'Ceremony' || row.tag === 'Break' || row.tag === 'Project')}">
          <div class="left-panel">
            <span style="text-align: center">{{row.timeline}}</span>
            <div v-if="row.tag">{{row.tag}}</div>
          </div>
          <div class="right-panel">
            <p v-if="row.title" class="schedule-title" :class="{clickable: row.dialog}" @click="dialogOpen(dateIdx, idx)">{{row.title}}</p>
            <p class="schedule-content" :class="{clickable: row.agendaChooseNum}" @click="nameClick(row)">{{row.content}}</p>
          </div>
        </div>
        <div class="body row">
          <div class="left-panel"></div>
          <div class="right-panel"></div>
        </div>
      </div>
    </div>
    <Modal v-if="isModalShow" @displayReset="isModalShow = false" :titleName="'Tentative Abstract'">
      <p class="modal-text">{{calenders[selectedDateId].body[selectedEventId].dialog}}</p>
    </Modal>
  </div>
</template>

<script>
import calenders from '@/static/agenda';
import Modal from './Modal';
export default {
  data() {
    return {
      calenders,
      currentSelect: 1,
      selectedDateId: -1,
      selectedEventId: -1,
      isModalShow: false
    }
  },
  components: { Modal },
  methods: {
    isSelected(id) {
      return id === this.currentSelect;
    },
    dialogOpen(dateId, eventId) {
      if (!calenders[dateId].body[eventId].dialog) return;
      this.selectedDateId = dateId;
      this.selectedEventId = eventId;
      this.isModalShow = true;
    },
    changeUrl(webUrl) {
      if (webUrl) window.location = webUrl;
    },
    nameClick(rowData) {
      if (!rowData.agendaChooseNum) return;
      this.$emit('nameClick', rowData.agendaChooseNum);
    }
  }
}
</script>

<style lang="scss" scoped>
$orange: #f66649;
$gray: #e6e6e6;

.timeline-wrapper {
  width: 100vw;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: $gray;
  position: relative;
  margin-top: 100px;
  .modal-text {
    width: 90%;
    line-height: 30px;
  }
  &:before {
    content:"\A";
    border-style: solid;
    border-width: 90px 100vw 0 0;
    border-color: transparent $gray transparent transparent;
    position: absolute;
    top:-90px;
  }
  .header {
    display: flex;
    flex-direction: row;
    align-items: center;
    z-index: 1;
    img {
      margin-right: 20px;
    }
    h2 {
      font-size: 2em;
      letter-spacing: 5px;
      color: rgb(54, 93, 150);
    }
  }
  .select-bar {
    width: 70%;
    .el-button {
      width: calc(100% / 4);
    }
  }
  .content {
    background-color: $gray;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 30px 0;
    position: relative;
    .calender {
      width: 80%;
      background-color: #fff;
      display: flex;
      flex-direction: column;
      margin-bottom: 30px;
      .row {
        width: 100%;
        height: 120px;
        display: flex;
        flex-direction: row;
        &.thinner {
          height: 100px;
        }
        .left-panel {
          width: 30%;
          height: 100%;
          background-color: rgba($orange,.28);
          display: flex;
          flex-direction: column;
          align-items: center;
          justify-content: center;

          color: $orange;
          letter-spacing: .1em;

          div {
            margin-top: 10px;
            border: 1px solid $orange;
            border-radius: 13px;
            padding: 3px 10px;
            font-size: .7em;
          }
        }
        .right-panel {
          width: 70%;
          height: 100%;

          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: center;
          padding: 0 5%;
          .calender-title {
            font-size: 1.5em;
            font-weight: 500;
            position: relative;
            top: 20px;
          }
          .calender-theme {
            font-size: 1.1em;
            font-weight: 500;
            margin-top: 10px;
            color: $orange;
            position: relative;
            top: 20px;
          }
          p {
            text-align: center;
            margin: 0;
            &.schedule-title {
              margin-bottom: 10px;
              color: #365d96;
            }
            &.clickable {
              cursor: pointer;
            }
          }
        }
        &.theme-row {
          height: 60px !important;
        }
      }
    }
  }
}

@media all and (min-width: 1220px) {
  .timeline-wrapper {
    font-size: 1.2em;
  }
}

@media all and (min-width: 580px) {
  .mobile {
    display: none;
  }
}

@media all and (max-width: 580px) {
  .timeline-wrapper {
    font-size: .8em;
  }
  .desktop {
    display: none;
  }
  .el-button-group {
    margin: 5px 0;
    .el-button {
      width: calc(100% / 2) !important;
    }
  }
}
</style>

