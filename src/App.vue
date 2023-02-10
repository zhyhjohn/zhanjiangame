<template>
    <div class="cover">
      <div class="main">
        <div class="content">
          <MyHeader />
          <MyPage />
        </div>
      </div>
    </div>
    <div class="footer">
      <MyFooter />
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
  .main {
    margin: 0 300px 0 150px;
    .content {
      height: 800px;
    }
  }
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
</style>
