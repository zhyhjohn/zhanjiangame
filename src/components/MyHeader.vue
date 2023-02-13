<template>
  <div class="top">
    <div class="icon">
      <a style="cursor: pointer" href="http://wowsgame.cn"
        ><img class="iconleft" src="../assets/anchor.png" alt="" />{{
          iconname
        }}</a
      >
      <span style="color: gray; padding: 0 20px"> | </span>
      <div class="icontxt">
        <img class="iconright" src="../assets/gameicon.png" alt="" />{{
          icontxt
        }}
      </div>
    </div>

    <div class="navs">
      <ul class="nav">
        <li
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

      <div class="login" @click="login()">
        <img class="loginpic" src="../assets/soldier.png" alt="" />
        <div class="loginbtn">注册/登录</div>
      </div>
    </div>
    <img class="agewarn" src="../assets/agewarning.png" alt="" />
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
.top {
  display: flex;
  justify-content: space-between;
  padding-top: 50px;
  .agewarn {
    position: absolute;
    width: 35px;
    height: 45px;
    top: 500px;
    cursor: pointer;
  }
  .icon {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    fill: currentColor;
    font-size: 25px;
    .iconleft {
      vertical-align: middle;
      width: 30px;
      height: 30px;
    }
    .icontxt {
      display: flex;
      align-items: center;
      background-image: linear-gradient(to right, #8effc6, #8eff8e, #ffff8e);
      -webkit-background-clip: text;
      color: transparent;
      font-size: 25px;
      .iconright {
        vertical-align: middle;
        width: 35px;
        height: 35px;
      }
    }
  }
  .navs {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 550px;
    .nav {
      display: flex;
    }
    .login {
      display: flex;
      align-items: center;
      color: #fff;
      margin-left: 0;
      .loginpic {
        display: flex;
        width: 20px;
        height: 20px;
        margin-left: 20px;
      }
      .loginbtn {
        margin-left: 15px;
        color: #fff;
        opacity: 0.6;
        font-size: 12px;
        cursor: pointer;
      }
    }
  }
}
a {
  color: white;
  text-decoration: none;
}
li {
  position: relative;
  color: white;
  list-style: none;
  margin-left: 50px;
  font-size: 14px;
  font-weight: bold;
  cursor: pointer;
}
</style>
