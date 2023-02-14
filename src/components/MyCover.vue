<template>
  <video class="videobg" autoplay loop muted src="../assets/wowsbg.mp4"></video>
  <div class="cover"></div>
</template>

<script>
export default {
  name: "MyCover",
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.videobg {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.cover {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 9;
  background: url(../assets/bgshadow.png);
  background-repeat: no-repeat;
  background-size: 100% 100%;
}
</style>