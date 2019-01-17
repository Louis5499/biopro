<template>
  <div class="modal" @click.self="displayReset(false)">
    <div class="popout">
      <div class="titlebar">
        <h2 class="titlebarText">
          <span>{{titleName}}</span>
        </h2>
        <div class="titlebarLine"></div>
        <img @click.self="displayReset(false)" class="titlebarCancel" src="@/assets/icon_cancel.svg" width="20px">
      </div>
      <div class="body">
        <slot />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentTab: 1
    };
  },
  props: {
    titleName: {
      type: String,
      default: 'bio'
    }
  },
  methods: {
    displayReset(arg) {
      if (typeof arg === 'number') {
        this.currentTab = arg;
      } else this.$emit('displayReset', false);
    }
  }
};
</script>

<style lang="scss" scoped>
@keyframes popouts {
  0% {
    transform: scale(0.9, 0.9);
  }
  100% {
    transform: scale(1, 1);
  }
}
@keyframes bgcfade {
  0% {
    background-color: rgba(28, 28, 28, 0);
  }
  100% {
    background-color: rgba(28,28,28,0.5);
  }
}
.modal {
  background-color: rgba(28,28,28,0.5);
  width: 100vw;
  height: 100vh;

  position: fixed;
  top: 0;
  left: 0;
  z-index: 587;

  display: flex;
  align-items: center;
  justify-content: center;
  animation: bgcfade .3s ease;

  transform: translate3d(0px, 0px, 0px);
}
.popout {
  width: 70vw;
  height: 50vw;
  overflow: hidden;
  background-color: #F6F6F6;

  max-width: 900px;
  max-height: 600px;
  animation: popouts .3s ease;

  z-index: 1001;

  position: relative;

  display: flex;
  flex-direction: column;
  align-items: center;
}
.titlebar {
  position: relative;
  width: 100%;
  min-height: 80px;

  display: flex;
  align-items: center;
  flex-direction: column;
}
.titlebarText{
  color: #333;
  font-weight: 500;
  font-size: 1.5em;
  margin-top: 20px;
}
.titlebarLine {
  width: 95%;
  height: 1px;
  background-color: #868686;
  margin-top: 10px;
}
.body {
  width: 100%;
  height: calc(100% - 70px);

  display: flex;
  flex-direction: column;
  align-items: center;

  overflow-y: scroll;
}
.titlebarCancel {
  position: absolute;
  right: calc(7% - 10px);
  top: 40%;
  transform: translate(-50%,-50%);

  cursor: pointer;
}
</style>
