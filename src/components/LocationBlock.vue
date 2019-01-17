<template>
  <div class="location-wrapper">
    <div class="map-block">
      <!-- <iframe width="100%" height="100%" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="https://www.openstreetmap.org/export/embed.html?bbox=120.98391294479372%2C24.78800079239005%2C121.00537061691284%2C24.802571482206947&amp;layer=mapnik&amp;marker=24.795282774950017%2C120.99464672617614"></iframe> -->
      <div id="map"></div>
      <!-- <iframe src="https://www.google.com/maps/embed?pb=!1m16!1m12!1m3!1d15016.321827465377!2d120.98782123626226!3d24.794423654458303!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!2m1!1z5riF5aSnIOaXuuWuj-mkqA!5e0!3m2!1szh-TW!2stw!4v1539604546691" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe> -->
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
          <p>To make sure you will not miss any interesting event, we provide the service of accommodation booking for participants (500NTD/person/night; Only 20 vacancies are available).</p>
          <p>You can purchase the accommodation tickets from the ticket page.</p>
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
  mounted() {
    function initMap() {
      var locationRio = { lat: 24.794525, lng: 120.992514 };
      var map = new google.maps.Map(document.getElementById('map'), {
        zoom: 13,
        center: locationRio,
        gestureHandling: 'cooperative'
      });
      var marker = new google.maps.Marker({
        position: locationRio,
        map: map,
        title: '清華大學'
      });
    };

    setTimeout(() => {
      initMap();
    }, 1000);
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
    #map {
      width: 100%;
      height: 100%;
    }
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
