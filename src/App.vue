<template>
  <div id="app">
    <TopBanner />
    <ThriveBlock />
    <TimelineBlock />
    <SpeakerBlock />
    <PosterBlock />
    <LocationBlock />
    <SponserBlock />
  </div>
</template>

<script>
import TopBanner     from '@/components/TopBanner';
import ThriveBlock   from '@/components/ThriveBlock';
import TimelineBlock from '@/components/TimelineBlock';
import SpeakerBlock  from '@/components/SpeakerBlock';
import PosterBlock   from '@/components/PosterBlock';
import LocationBlock from '@/components/LocationBlock';
import SponserBlock  from '@/components/SponserBlock';

export default {
  name: 'App',
  components: {
    TopBanner, ThriveBlock, TimelineBlock, SpeakerBlock, PosterBlock, LocationBlock, SponserBlock
  }
}
</script>

<style lang="scss">
@import url(//fonts.googleapis.com/earlyaccess/notosanstc.css);
#app {
  display: flex;
  flex-direction: column;
  font-family: 'Noto Sans TC', sans-serif;
  width: 100vw;
}
</style>
