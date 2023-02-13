<template>
  <div class="layer"></div>
  <div class="container" ref="appref">
    <MyCover />
    <div class="main">
      <div class="content">
        <MyHeader />
        <MyPage />
      </div>
      <MyFooter />
    </div>
  </div>
</template>

<script setup>
import MyHeader from "./components/MyHeader";
import MyPage from "./components/MyPage";
import MyFooter from "./components/MyFooter";
import MyCover from "./components/MyCover";
</script>

<style lang="scss" scoped>
.layer {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: #000;
  opacity: 1;
}
.container {
  .main {
    .content {
      position: relative;
      margin: 0 300px 0 150px;
      height: 800px;
      z-index: 99;
    }
  }
}

#app {
  height: 100%;
}
</style>
