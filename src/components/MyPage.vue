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
        style="width: 300px; height: 40px"
        src="../assets/infotop.png"
        alt=""
      />
    </div>
    <div class="step">
      <div class="step1">
        <img
          style="width: 40px; height: 40px; margin-top: 20px"
          src="../assets/numberone.png"
          alt=""
        />
        <div class="desc" @click="login()">
          <h4>快速注册<br />360账号</h4>
        </div>
      </div>
      <div class="step2">
        <img
          style="width: 40px; height: 40px; margin-top: 20px"
          src="../assets/numbertwo.png"
          alt=""
        />
        <div class="desc" @click="login()">
          <h4>免下载<br />登录即玩</h4>
        </div>
      </div>
      <div class="step3">
        <img
          style="width: 40px; height: 40px; margin-top: 20px"
          src="../assets/numberthree.png"
          alt=""
        />
        <div class="desc" @click="login()">
          <h4>免费畅玩<br />开启云海战时代</h4>
        </div>
      </div>
    </div>
    <div class="gamebtn" @click="login()">
      点击立即开战
      <div class="tip"></div>
    </div>
    <div class="read">
      <input type="radio" />我已阅读，并确认理解和接受
      <a href="https://wg.360.cn/user/agreement/list.html"
        >《360游戏服务及许可协议》,《360用户隐私政策》,《360儿童隐私保护政策》</a
      >
    </div>
    <div class="download">
      <a href="https://redir.wggames.cn/z799nl95/"
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
        style="width: 60px; height: 15px"
        src="../assets/yuanjing.png"
        alt=""
      />
      提供云游戏技术服务
    </div>
  </div>
  <div class="submit"></div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "MyPage",
  setup() {
    let qqnumber = ref(677940959);

    function login() {
      alert("请先注册登录");
    }

    return { qqnumber, login };
  },
};
</script>
<style lang="less" scoped>
.agewarn {
  float: left;
  margin-left: 150px;
  margin-top: 400px;
}
.container {
  width: 700px;
  float: right;
  .info {
    margin-right: 400px;
    float: right;
  }
  .step {
    margin-top: 20px;
    margin-right: 250px;
    width: 450px;
    height: 50px;
    float: right;
    cursor: pointer;

    .step1,
    .step2,
    .step3 {
      padding-left: 20px;
      background: linear-gradient(to right, rgb(100, 100, 100), transparent);
      margin-right: 10px;
      float: left;
      clip-path: polygon(100% -200%, 100% 100%, 20% 100%, 0% 50%);

      .desc {
        text-align: left;
        color: white;
        float: right;
      }
    }
  }
  .gamebtn {
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    border-radius: 10px;
    background-color: red;
    text-align: center;
    font-size: 20px;
    color: white;
    width: 250px;
    height: 60px;
    margin-right: 450px;
    margin-top: 50px;
    float: right;
    cursor: pointer;
    .tip {
      position: absolute;
      color: white;
    }
  }
  .read {
    margin-top: 10px;
    width: 400px;
    height: 60px;
    float: right;
    color: white;
    margin-right: 310px;
  }
  .download {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-right: 450px;
    margin-top: 20px;
    border-radius: 10px;
    background-color: rgba(203, 153, 45, 0.5);
    font-size: 10px;
    width: 250px;
    height: 40px;
    float: right;
  }
  .joingroup {
    margin-top: 10px;
    margin-right: 300px;
    font-size: 10px;
    width: 400px;
    height: 40px;
    color: white;
    float: right;
  }
  .whoprovide {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-right: 410px;
    font-size: 10px;
    width: 400px;
    height: 40px;
    color: white;
    float: right;
  }
}
a {
  color: white;
  text-decoration: none;
}
</style>
