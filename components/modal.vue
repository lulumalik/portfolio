<template>
  <div class="mainModalTransparent">
    <div class="mainModal" @click="close"></div>
    <div class="bgModal">
      <div class="closeButton" @click="close">&times;</div>
      <div>
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    close(e) {
      this.$emit("close", e);
    }
  }
};
</script>

<style scoped>
.closeButton {
  font-size: 25px;
  position: absolute;
  right: 15px;
  top: 0px;
  cursor: pointer;
}
.vertical-center {
  margin: 0px auto;
  position: absolute;
  top: 50%;
  right: 0px;
  left: 0px;
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
}
.mainModal {
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  text-align: center;
  position: fixed;
  z-index: 1001;
  top: 0px;
  left: 0px;
  background: rgba(0, 0, 0, 0.5);
}
.mainModalTransparent {
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  text-align: center;
  position: fixed;
  z-index: 100000;
}

.bgModal {
  position: fixed;
  animation: fadeIn; /* referring directly to the animation's @keyframe declaration */
  animation-duration: 0.5s;
  top: 50%;
  transform: translateY(-50%);
  left: 0;
  right: 0;
  margin: 0px auto;
  padding: 15px;
  margin-right: 10px;
  margin-left:10px;
  max-height: 90vh;
  min-height: 150px;
  overflow-y: auto;
  border-radius: 10px;
  z-index: 1002;
  background: white;
}
</style>