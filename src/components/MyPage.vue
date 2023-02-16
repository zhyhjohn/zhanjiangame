<template>
  <div class="info_container">
    <img class="info" src="../assets/infotop.png" alt="" />
    <div class="step">
      <div class="step1">
        <img class="step-pic" src="../assets/numberone.png" alt="" />
        <div class="desc" @click="logintip()">
          <span class="step-desc">快速注册</span><span class="step-desc">360账号</span>
        </div>
      </div>
      <div class="step2">
        <img class="step-pic" src="../assets/numbertwo.png" alt="" />
        <div class="desc" @click="logintip()">
          <span class="step-desc">免下载</span>
          <span class="step-desc">登录即玩</span>
        </div>
      </div>
      <div class="step3">
        <img class="step-pic" src="../assets/numberthree.png" alt="" />
        <div class="desc" @click="logintip()">
          <span class="step-desc">免费畅玩</span>
          <span class="step-desc">开启云海战时代</span>
        </div>
      </div>
    </div>
    <div class="start-btn">
      <div class="game-btn" @click="logintip()">
        <div class="tip">官方云游戏</div>
      </div>
    </div>
    <div class="read">
      <input type="checkbox" />
      <p>
        我已阅读，并确认理解和接受
        <a class="read-text"
          href="https://wg.360.cn/user/agreement/list.html">《360游戏服务及许可协议》,《360用户隐私政策》,《360儿童隐私保护政策》</a>。
      </p>
    </div>
    <div class="download">
      <img src="https://s0.ssl.qhres2.com/static/0336c86998e26823.svg" alt="" />
      <a class="download-text" href="https://redir.wggames.cn/z799nl95/">下载《战舰世界》客户端
        无限畅玩</a>
    </div>
    <div class="joingroup">
      <p>
        战舰世界云游戏官方QQ群：<a class="number" href="https://jq.qq.com/?_wv=1027&k=PqUG6vtg">{{ qqnumber }} 点击加入</a>
      </p>
    </div>
    <div class="whoprovide">
      <img class="whopic" src="../assets/yuanjing.png" alt="" />
      <span class="whotext">提供云游戏技术服务</span>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { ElMessage } from "element-plus";

let qqnumber = ref(677940959);
const logintip = () => {
  ElMessage.error("请先登陆账号！");
};
</script>

<style lang="scss" scoped>
@mixin stepitem {
  display: flex;
  align-items: center;
  width: 180px;
  height: 70px;
  padding-left: 20px;
  background-repeat: no-repeat;
  background-size: 100% 100%;

  .step-pic {
    width: 25px;
    height: 40px;
  }

  .desc {
    display: flex;
    flex-direction: column;
    margin-left: 10px;
    font-size: 14px;
    color: white;

    .step-desc {
      display: block;
      width: 100px;
    }
  }
}

.info_container {
  position: absolute;
  width: 600px;
  top: 220px;
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
    margin-bottom: 65px;
    cursor: pointer;

    .step1 {
      background: url(../assets/steppic1.png);
      @include stepitem;
    }

    .step2 {
      background: url(../assets/steppic2.png);
      @include stepitem;
      transform: translate(-20px);
    }

    .step3 {
      @extend .step2;
      transform: translate(-40px);
    }
  }

  .start-btn {
    display: flex;
    margin-left: 30px;
    align-items: center;
    cursor: pointer;

    .game-btn {
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
        color: #000;
        font-size: 18px;
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

    .read-text {
      color: #d6fffb;

      &:hover {
        color: #8ffaef;
      }
    }
  }

  .download {
    display: inline-flex;
    width: 400px;
    height: 40px;
    margin-top: 30px;
    margin-bottom: 10px;
    margin-left: 30px;
    background: rgba(255, 186, 125, 0.4);
    border-radius: 5px;
    border: 1px solid rgba(255, 210, 157, 0.32);
    font-size: 16px;
    color: #fff3b8;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    transition: all 0.3s;

    &:hover {
      background: rgba(245, 150, 65, 0.4);
    }

    .download-text {
      color: #fff3b8;
      padding: 5px;
      display: block;
    }
  }

  .joingroup {
    width: 400px;
    margin-left: 30px;
    margin-bottom: 15px;
    line-height: 20px;
    font-size: 16px;

    .number {
      color: #fff;
      opacity: 0.7;

      &:hover {
        opacity: 1;
      }
    }
  }

  .whoprovide {
    display: flex;
    margin-top: 20px;
    margin-left: 30px;
    font-size: 16px;
    align-items: center;

    .whopic {
      width: 65px;
      height: 20px;
      margin: 5px;
      opacity: 0.7;
    }

    .whotext {
      font-size: 14px;
      color: #fff;
      opacity: 0.4;
      user-select: none;
    }
  }
}

a {
  color: #fff;
  text-decoration: none;
}
</style>
