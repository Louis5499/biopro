<template>
  <div class="wrapper">
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
  components: {
    TopBanner, ThriveBlock, TimelineBlock, SpeakerBlock, PosterBlock, LocationBlock, SponserBlock
  }
}
</script>

<style lang="scss" scoped>

</style>
