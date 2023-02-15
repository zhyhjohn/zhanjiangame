<template>
  <div class="video">
    <video class="videobg" autoplay loop muted src="../assets/wowsbg.mp4"></video>
    <div class="cover"></div>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;

  .videobg {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .cover {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    z-index: 9;
    background: url(../assets/bgshadow.png);
    background-repeat: no-repeat;
    background-size: 100% 100%;
  }
}
</style>