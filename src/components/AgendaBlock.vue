<template>
  <div class="agenda-wrapper">
    <div class="header">
      <img src="@/assets/icon_agenda.svg" width="30px" />
      <h2 class="title">Agenda</h2>
    </div>
    <div class="content">
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="scss" scoped>
.agenda-wrapper {
  width: 100vw;
  display: flex;
  flex-direction: column;
  align-items: center;
  .header {
    display: flex;
    flex-direction: row;
    align-items: center;
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
    display: flex;
    justify-content: center;
    width: 100vw;
    flex-wrap: wrap;
  }
}
</style>
