<template>
  <div class="infocontainer">
    <img class="info" src="../assets/infotop.png" alt="" />
    <div class="step">
      <div class="step1">
        <img class="steppic" src="../assets/numberone.png" alt="" />
        <div class="desc" @click="login()">
          <span class="stepdesc">快速注册</span
          ><span class="stepdesc">360账号</span>
        </div>
      </div>
      <div class="step2">
        <img class="steppic" src="../assets/numbertwo.png" alt="" />
        <div class="desc" @click="login()">
          <span class="stepdesc">免下载</span>
          <span class="stepdesc">登录即玩</span>
        </div>
      </div>
      <div class="step3">
        <img class="steppic" src="../assets/numberthree.png" alt="" />
        <div class="desc" @click="login()">
          <span class="stepdesc">免费畅玩</span>
          <span class="stepdesc">开启云海战时代</span>
        </div>
      </div>
    </div>
    <div class="startbtn">
      <div class="gamebtn" @click="login()">
        <div class="tip">官方云游戏</div>
      </div>
    </div>
    <div class="read">
      <input type="radio" />
      <p>
        我已阅读，并确认理解和接受
        <a
          style="color: #d6fffb"
          href="https://wg.360.cn/user/agreement/list.html"
          >《360游戏服务及许可协议》,《360用户隐私政策》,《360儿童隐私保护政策》</a
        >
      </p>
    </div>
    <div class="download">
      <img src="https://s0.ssl.qhres2.com/static/0336c86998e26823.svg" alt="" />
      <a
        style="color: #fff3b8; padding: 5px; display: block"
        href="https://redir.wggames.cn/z799nl95/"
        >下载《战舰世界》客户端 无限畅玩</a
      >
    </div>
    <div class="joingroup">
      <p>
        战舰世界云游戏官方QQ群：<a href="https://jq.qq.com/?_wv=1027&k=PqUG6vtg"
          >{{ qqnumber }} 点击加入</a
        >
      </p>
    </div>
    <div class="whoprovide">
      <img
        style="width: 75px; height: 25px"
        src="../assets/yuanjing.png"
        alt=""
      />
      提供云游戏技术服务
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
let qqnumber = ref(677940959);

function login() {
  alert("请先注册登录");
}
</script>
<style lang="scss" scoped>
@mixin step {
  display: flex;
  align-items: center;
  width: 150px;
  height: 60px;
  padding-left: 20px;
  background-repeat: no-repeat;
  background-size: 100% 100%;
  .steppic {
    width: 25px;
    height: 40px;
  }
  .desc {
    display: flex;
    flex-direction: column;
    margin-left: 10px;
    font-size: 14px;
    color: white;
    .stepdesc {
      display: block;
      width: 100px;
    }
  }
}

.infocontainer {
  position:absolute;
  width: 550px;
  top: 200px;
  right: 0;
  color: #fff;
  .info {
    width: 450px;
    height: 50px;
    margin-left: 30px;
    margin-bottom: 28px;
  }
  .step {
    display: flex;
    margin-left: 30px;
    margin-bottom: 80px;
    cursor: pointer;

    .step1 {
      background: url(../assets/steppic1.png);
      @include step;
    }
    .step2 {
      background: url(../assets/steppic2.png);
      @include step;
          transform: translate(-20px);
    }
    .step3 {
      background: url(../assets/steppic2.png);
      @include step;
      transform: translate(-40px);
    }
  }
  .startbtn {
    display: flex;
    align-items: center;
    margin-left: 30px;
    cursor: pointer;
    .gamebtn {
      width: 400px;
      height: 110px;
      background: url(../assets/startbtn.png);
      background-repeat: no-repeat;
      background-size: 100% 100%;
      .tip {
        width: 100px;
        height: 30px;
        margin: 1px 0 0 1px;
        padding-left: 10px;
        background: url(../assets/gamebtntip.png);
        background-repeat: no-repeat;
        background-size: 100% 100%;
        font-size: 18px;
        color: #000;
        line-height: 28px;
      }
    }
  }
  .read {
    display: flex;
    align-items: center;
    margin-left: 30px;
    font-size: 16px;
    opacity: 0.7;
  }
  .download {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 400px;
    height: 40px;
    margin-top: 30px;
    margin-bottom: 15px;
    margin-left: 30px;
    background: rgba(255, 186, 125, 0.4);
    border-radius: 5px;
    border: 1px solid rgba(255, 210, 157, 0.32);
    font-size: 16px;
    color: #fff3b8;
  }
  .joingroup {
    width: 400px;
    margin-left: 30px;
    margin-bottom: 15px;
    line-height: 20px;
    font-size: 16px;
  }
  .whoprovide {
    display: flex;
    align-items: center;
    margin-top: 20px;
    margin-left: 30px;
    font-size: 16px;
  }
}
a {
  color: #fff;
  text-decoration: none;
}
</style>
