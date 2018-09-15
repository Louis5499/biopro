<template>
  <div class="timeline-wrapper">
    <div class="header">
      <img src="@/assets/icon_clock.svg" width="30px"/>
      <h2 class="title">Timeline</h2>
    </div>
    <div class="content">
      <div class="calender" v-for="(calender, idx) in calenders" :key="idx">
        <div class="title row">
          <div class="left-panel"></div>
          <div class="right-panel">
            <span class="calender-title">{{calender.title}}</span>
          </div>
        </div>
        <div class="body row" v-for="(row, idx) in calender.body" :key="idx">
          <div class="left-panel">
            <span>{{row.timeline}}</span>
            <div v-if="row.tag">{{row.tag}}</div>
          </div>
          <div class="right-panel">
            <p v-if="row.title" class="schedule-title">{{row.title}}</p>
            <p class="schedule-content">{{row.content}}</p>
          </div>
        </div>
        <div class="body row">
          <div class="left-panel"></div>
          <div class="right-panel"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      calenders: [
        {
          title: 'Day One 1/16',
          body: [
            {
              timeline: '08:00 - 08:30',
              content: `Register` 
            },
            {
              timeline: '08:00 - 08:30',
              tag: 'Seminar',
              title: `Viewing Bigger Pictures Promotes Happier Mood: A psychological explanation and an example in the wild`,
              content: `Prof. Xuefeng Liang, Kyoto University, Japan` 
            },
            {
              timeline: '08:00 - 08:30',
              tag: 'Seminar',
              title: `Viewing Bigger Pictures Promotes Happier Mood: A psychological explanation and an example in the wild`,
              content: `Prof. Xuefeng Liang, Kyoto University, Japan` 
            }
          ]
        },
        {
          title: 'Day Two 1/17',
          body: [
            {
              timeline: '08:00 - 08:30',
              tag: 'Seminar',
              title: `Viewing Bigger Pictures Promotes Happier Mood: A psychological explanation and an example in the wild`,
              content: `Prof. Xuefeng Liang, Kyoto University, Japan` 
            },
            {
              timeline: '08:00 - 08:30',
              tag: 'Seminar',
              title: `Viewing Bigger Pictures Promotes Happier Mood: A psychological explanation and an example in the wild`,
              content: `Prof. Xuefeng Liang, Kyoto University, Japan` 
            },
            {
              timeline: '08:00 - 08:30',
              tag: 'Seminar',
              title: `Viewing Bigger Pictures Promotes Happier Mood: A psychological explanation and an example in the wild`,
              content: `Prof. Xuefeng Liang, Kyoto University, Japan` 
            }
          ]
        }
      ]
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
          }
          p {
            text-align: center;
            margin: 0;
            &.schedule-title {
              margin-bottom: 10px;
              color: #365d96;
            }
          }
        }
      }
    }
  }
}
</style>

