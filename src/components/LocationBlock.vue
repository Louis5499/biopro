<template>
  <div class="location-wrapper">
    <div class="map-block">
      <iframe width="100%" height="100%" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="https://www.openstreetmap.org/export/embed.html?bbox=120.98391294479372%2C24.78800079239005%2C121.00537061691284%2C24.802571482206947&amp;layer=mapnik&amp;marker=24.795282774950017%2C120.99464672617614"></iframe>
    </div>
    <div class="word-block">
      <div class="theme-block">
        <div class="theme-title">Location</div>
        <div class="theme-description">
          <p>Room, MXIC Building(School Library) 3F</p>
          <p>National Tsing Hua University</p>
          <p>No.101, Sec. 2, Guangfu Rd., East Dist., Hsinchu City 300, Taiwan</p>
        </div>
      </div>
      <div class="theme-block">
        <div class="theme-title">Accomadation</div>
        <div class="theme-description">
          <p>To make sure you will not miss any interesting event, we provide the service of accommodation booking for participants (600NTD/person/night; Only 20 vacancies are available).</p>
          <p>You can purchase the one-night(1/26 ~ 1/27) or two-night (1/26 ~ 1/28) tickets from the ticket page.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  methods: {

  }
}
</script>

<style lang="scss" scoped>
.location-wrapper {
  height: 700px;
  .map-block {
    position: relative;
    top: -2vw;
    height: 50%;
  }
  .word-block {
    display: flex;
    flex-direction: row;
    .theme-block {
      display: flex;
      flex-direction: column;

      padding: 0 5%;
      width: 50%;
      p {
        margin: 5px 0;
      }
      .theme-title {
        color: #3c5d97;
        font-size: 2em;
      }
      .theme-description {
        display: flex;
        flex-direction: column;
      }
    }
  }
}
</style>
