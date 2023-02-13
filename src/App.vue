<template>
  <div class="cover">
    <div class="video">
      <video autoplay loop muted src="./assets/wowsbg.mp4"></video>
    </div>
    <div class="main">
      <MyHeader />
      <MyPage />
    </div>
    <div class="footer">
      <MyFooter />
    </div>
  </div>
</template>

<script>
import MyHeader from "./components/MyHeader";
import MyPage from "./components/MyPage";
import MyFooter from "./components/MyFooter";

export default {
  name: "App",
  components: {
    MyHeader,
    MyPage,
    MyFooter,
  },
};
</script>

<style lang="scss" scoped>
.cover {
  background: url(https://p1.ssl.qhimg.com/t012aaa7efa80a1f624.png);
  background-repeat: no-repeat;
  background-size: 100% 100%;
  .video {
    position: fixed;
    width: auto;
    height: auto;
    top: 50%;
    left: 50%;
    min-width: 100%;
    min-height: 100%;
    z-index: -100;
    transform: translateX(-50%) translateY(-50%);
    transition: 1s opacity;
  }

  .main {
    position: relative;
    margin: 0 300px 0 150px;
    height: 750px;
  }
  .footer {
    background-color: #000000;
    width: 100%;
    padding: 20px 0;
    position: fixed;
    bottom: 0;
    left: 0;
  }
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
