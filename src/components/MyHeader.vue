<template>
  <div class="container">
    <div class="video">
      <video autoplay loop muted src="../assets/wowsbg.mp4"></video>
    </div>
    <div class="top">
      <div class="icon">
        <a style="cursor: pointer" href="http://wowsgame.cn"
          ><img
            style="vertical-align: middle; width: 30px; height: 30px;"
            src="../assets/anchor.png"
            alt=""
          />{{ iconname }}</a
        >
        <span style="color: gray"> | </span>
        <div class="icontxt">
          <img
            style="vertical-align: middle; width: 35px; height: 35px;"
            src="../assets/gameicon.png"
            alt=""
          />{{ icontxt }}
        </div>
      </div>

      <div class="nav">
        <ul>
          <li
            style="
              cursor: pointer;
              font-family: PingFangSC-Regular, PingFang SC;
            "
            @click="login()"
            :class="{ active: index === 0 }"
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
          style="
            vertical-align: middle;
            width: 28px;
            height: 28px;
            padding-right: 15px;
          "
          src="../assets/soldier.png"
          alt=""
        />注册/登录
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, reactive } from "vue";

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
</script>

<style lang="scss" scoped>
.active {
  color: #25ffa9;
}
.container {
  padding-top: 30px;
  .top {
    width: 1500px;
    height: 120px;
    text-align: center;
    .icon {
      margin: {
        top: 15px;
        left: 150px;
      }
      width: 300px;
      height: 100px;
      float: left;
      font-size: 25px;
      .icontxt {
        float: right;
        background-image: linear-gradient(to right, #8effc6, #8eff8e, #ffff8e);
        -webkit-background-clip: text;
        color: transparent;
        font: {
          size: 25px;
          font-weight: bold;
        }
      }
    }
    .nav {
      margin: {
        top: 10px;
        left: 230px;
      }
      width: 200px;
      height: 100px;
      float: left;
    }
    .login {
      margin: {
        top: 18px;
        left: 300px;
      }
      width: 100px;
      height: 50px;
      color: white;
      font-size: 12px;
      float: left;
      cursor: pointer;
    }
  }
}
video {
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
a {
  color: white;
  text-decoration: none;
}
ul {
  display: -webkit-box;
}
li {
  color: white;
  width: 60%;
  float: right;
  list-style: none;
  font: {
    size: 14px;
    weight: bold;
  }
}
</style>
