<template>
  <div class="video">
    <video
      class="videobg"
      autoplay
      loop
      muted
      src="../assets/wowsbg.mp4"
    ></video>
    <div class="cover"></div>
  </div>
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
.video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 800px;
  .videobg {
    width: 100%;
    height: 800px;
    object-fit: cover;
  }
  .cover {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 800px;
    z-index: 9;
    background: url(../assets/bgshadow.png);
    background-repeat: no-repeat;
    background-size: 100% 100%;
  }
}
</style>