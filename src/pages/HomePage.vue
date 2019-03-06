<template>
  <div class="wrapper">
    <TopBanner />
    <ThriveBlock />
    <TimelineBlock @nameClick="agendaChooseNum = $event"/>
    <SpeakerBlock :agendaChooseNum="agendaChooseNum"/>
    <HandOnBlock />
    <!-- <AgendaBlock /> -->
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
import AgendaBlock   from '@/components/AgendaBlock';
import PosterBlock   from '@/components/PosterBlock';
import HandOnBlock   from '@/components/HandOnBlock';
import LocationBlock from '@/components/LocationBlock';
import SponserBlock  from '@/components/SponserBlock';

export default {
  components: {
    TopBanner, ThriveBlock, TimelineBlock, SpeakerBlock, AgendaBlock, PosterBlock, LocationBlock, SponserBlock, HandOnBlock
  },
  data() {
    return {
      agendaChooseNum: 0
    }
  }
}
</script>

<style lang="scss" scoped>
.wrapper {
  overflow: hidden;
  width: 100vw;
}
</style>
