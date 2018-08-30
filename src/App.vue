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
@import url('https://fonts.googleapis.com/css?family=Open+Sans');
#app {
  display: flex;
  flex-direction: column;
  font-family: 'Open Sans', sans-serif;
  width: 100vw;
}
html, body {
  margin: 0;
  padding: 0;
}
</style>
