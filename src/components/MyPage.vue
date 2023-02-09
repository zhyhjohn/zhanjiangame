<template>
  <div class="agewarn">
    <img
      style="width: 40px; height: 50px"
      src="../assets/agewarning.png"
      alt=""
    />
  </div>
  <div class="container">
    <div class="info">
      <img
        style="width: 380px; height: 40px"
        src="../assets/infotop.png"
        alt=""
      />
    </div>
    <div class="step">
      <div class="step1">
        <img
          style="width: 15px; height: 30px; margin-top: 10px"
          src="../assets/numberone.png"
          alt=""
        />
        <div class="desc" @click="login()">快速注册<br />360账号</div>
      </div>
      <div class="step2">
        <img
          style="width: 15px; height: 30px; margin-top: 10px"
          src="../assets/numbertwo.png"
          alt=""
        />
        <div class="desc" @click="login()">免下载<br />登录即玩</div>
      </div>
      <div class="step3">
        <img
          style="width: 15px; height: 30px; margin-top: 10px"
          src="../assets/numberthree.png"
          alt=""
        />
        <div class="desc" @click="login()">免费畅玩<br />开启云海战时代</div>
      </div>
    </div>
    <div class="gamebtn" @click="login()">
      <img
        style="width: 350px; height: 80px"
        src="../assets/startbtn.png"
        alt=""
      />
      <div class="tip">
        <img
          style="width: 85px; height: 20px"
          src="../assets/gamebtntip.png"
          alt=""
        />
        <span
          style="
            position: absolute;
            top: 2px;
            bottom: 0;
            left: 8px;
            color: #000;
            font-size: 12px;
          "
          >官方云游戏</span
        >
      </div>
    </div>
    <div class="read">
      <input type="radio" />我已阅读，并确认理解和接受
      <a
        style="color: #d6fffb"
        href="https://wg.360.cn/user/agreement/list.html"
        >《360游戏服务及许可协议》,《360用户隐私政策》,《360儿童隐私保护政策》</a
      >
    </div>
    <div class="download">
      <img src="https://s0.ssl.qhres2.com/static/0336c86998e26823.svg" alt="" />
      <a
        style="color: #fff3b8; padding: 5px"
        href="https://redir.wggames.cn/z799nl95/"
        >下载《战舰世界》客户端 无限畅玩</a
      >
    </div>
    <div class="joingroup">
      战舰世界云游戏官方QQ群：<a href="https://jq.qq.com/?_wv=1027&k=PqUG6vtg"
        >{{ qqnumber }} 点击加入</a
      >
    </div>
    <div class="whoprovide">
      <img
        style="width: 50px; height: 15px"
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
  width: 130px;
  height: 55px;
  padding-left: 20px;
  float: left;
  background-repeat: no-repeat;
  background-size: 100% 100%;
  .desc {
    width: 100px;
    height: 40px;
    margin-top: 10px;
    font-size: 12px;
    text-align: left;
    color: white;
    float: right;
  }
}

.agewarn {
  float: left;
  cursor: pointer;
  margin: {
    left: 150px;
    top: 450px;
  }
}
.container {
  margin-top: 20px;
  width: 600px;
  float: right;
  .info {
    margin-right: 300px;
    float: right;
  }
  .step {
    margin: {
      top: 20px;
      right: 180px;
    }
    width: 500px;
    height: 60px;
    float: right;
    cursor: pointer;

    .step1 {
      background: url(../assets/steppic1.png);
      @include step;
    }
    .step2,
    .step3 {
      background: url(../assets/steppic2.png);
      @include step;
    }
  }
  .gamebtn {
    margin: {
      right: 400px;
      top: 60px;
    }
    width: 250px;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    float: right;
    cursor: pointer;
    .tip {
      margin: {
        right: 219px;
        bottom: 55px;
      }
      position: absolute;
      color: white;
    }
  }
  .read {
    margin: {
      top: 15px;
      right: 230px;
    }
    width: 450px;
    height: 60px;
    float: right;
    font-size: 12px;
    color: white;
  }
  .download {
    margin: {
      top: 10px;
      right: 380px;
    }
    width: 300px;
    height: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 5px;
    color: #fff3b8;
    background-color: #ffba7d66;
    font-size: 12px;

    float: right;
  }
  .joingroup {
    margin: {
      top: 10px;
      right: 280px;
    }
    width: 400px;
    height: 25px;
    font-size: 10px;
    color: white;
    float: right;
  }
  .whoprovide {
    width: 400px;
    height: 30px;
    margin-right: 400px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 10px;
    color: white;
    float: right;
  }
}
a {
  color: white;
  text-decoration: none;
}
</style>
