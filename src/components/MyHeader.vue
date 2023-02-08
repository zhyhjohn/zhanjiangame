<template>
  <div class="container">
    <div class="video">
      <video autoplay loop muted src="../assets/wowsbg.mp4"></video>
    </div>
    <div class="top">
      <div class="icon">
        <a style="cursor: pointer" href="http://wowsgame.cn"
          ><img
            style="vertical-align: middle; width: 30px; height: 30px"
            src="../assets/anchor.png"
            alt=""
          />{{ iconname }}</a
        >
        <span style="color: gray"> | </span>
        <div class="icontxt">
          <img
            style="vertical-align: middle; width: 40px; height: 40px"
            src="../assets/gameicon.png"
            alt=""
          />{{ icontxt }}
        </div>
      </div>

      <div class="nav">
        <ul>
          <li
            style="cursor: pointer"
            @click="login()"
            @mouseenter="changeActive($event)"
            @mouseleave="removeActive($event)"
            v-for="(item, index) in navs"
            :key="index"
          >
            {{ item }}
          </li>
        </ul>
      </div>

      <div class="login" @click="login()">
        <img
          style="vertical-align: middle; width: 18px; height: 18px"
          src="../assets/soldier.png"
          alt=""
        />注册/登录
      </div>
    </div>
  </div>
</template>

<script>
import { ref, reactive } from "vue";
export default {
  name: "MyHeader",
  setup() {
    let iconname = ref("战舰世界");
    let icontxt = ref("云游戏");
    let navs = reactive(["首页", "意见反馈", "FAQ", "前往官网"]);

    function login() {
      alert("请先注册登录");
    }
    //鼠标触碰变色方法
    function changeActive(e) {
      e.currentTarget.className = "active";
    }
    function removeActive(e) {
      e.currentTarget.className = "";
    }

    return {
      iconname,
      icontxt,
      navs,
      login,
      changeActive,
      removeActive,
    };
  },
};
</script>

<style lang="less" scoped>
.active {
  color: #8eff8e;
}
.container {
  margin-top: 50px;

  .top {
    width: 1500px;
    height: 120px;
    text-align: center;
    .icon {
      margin-top: 15px;
      margin-left: 150px;
      width: 300px;
      height: 100px;
      float: left;
      font-size: 30px;
      .icontxt {
        float: right;
        margin-right: 0px;
        background-image: linear-gradient(to right, #8effc6, #8eff8e, #ffff8e);
        -webkit-background-clip: text;
        color: transparent;
        font-size: 30px;
      }
    }
    .nav {
      margin-left: 250px;
      width: 200px;
      height: 100px;
      float: left;
    }
    .login {
      color: white;
      margin-top: 15px;
      margin-left: 250px;
      float: left;
      width: 100px;
      cursor: pointer;
    }
  }
}
video {
  position: fixed;
  top: 50%;
  left: 50%;
  min-width: 100%;
  min-height: 100%;
  width: auto;
  height: auto;
  z-index: -100;
  transform: translateX(-50%) translateY(-50%);
  transition: 1s opacity;
}
a {
  color: white;
  text-decoration: none;
}
ul {
  display: -webkit-box;
}
li {
  color: white;
  width: 50%;
  float: right;
  font-size: 18px;
  list-style: none;
}
</style>
