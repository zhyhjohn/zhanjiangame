<template>
    <MyHeader />
    <MyPage />
    <MyFooter />
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

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  position: absolute;
}
</style>
