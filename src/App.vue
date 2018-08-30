<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App'
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
