<template>
  <div class="sponser-wrapper">
    <div class="directing-sponser">
      <span>Directing Insititute</span>
      <img src="@/assets/moe-logo.png" width="100px">
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="scss" scoped>
.sponser-wrapper {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  .directing-sponser {
    display: flex;
    flex-direction: column;
    align-items: center;
    span {
      margin-bottom: 20px;
    }
  }
}
</style>

