<template>
  <div class="top">
    <div class="icon">
      <a class="topicon" style="cursor: pointer" href="http://wowsgame.cn"><img class="iconleft"
          src="../assets/anchor.png" alt="" />{{
            iconname
          }}</a>
      <span class="iconline" style="color: gray; padding: 0 20px"> | </span>
      <div class="icontxt">
        <img class="iconright" src="../assets/gameicon.png" alt="" />{{
          icontxt
        }}
      </div>
    </div>

    <div class="navs">
      <ul class="nav">
        <li class="navitemfirst">首页</li>
        <li class="navitem" @click="logintip()">意见反馈</li>
        <li>
          <a class="navitem" href="https://camp.wot.360.cn/shipfaq.html">FAQ</a>
        </li>
        <li>
          <a class="navitem" href="https://wowsgame.cn/">前往官网</a>
        </li>
      </ul>

      <div class="login" @click="showlogin = true">
        <img class="loginpic" src="../assets/soldier.png" alt="" />
        <div class="loginbtn">注册/登录</div>
      </div>
    </div>
    <img class="agewarn" src="../assets/agewarning.png" alt="" @click="showwarning = true" />
  </div>
  <el-dialog class="agetxt" v-model="showwarning" title="" width="50%" top="10%">
    <span>
      <h1>《战舰世界》适龄提示</h1>
    </span><br /><br />
    <span class="agetxt">本游戏以20世纪前半叶造船工业的蓝图和影视资料为背景参考，以超清的3D建模和优秀的物理引擎高度还原战舰模型和海洋场景，
      游戏方式多样灵活，美术设计唯美写实、色彩鲜明，配乐风格多样，婉转悠扬。游戏中部分指挥官、地图场景和战舰外观有虚构的背景故事，
      但不会与现实相混淆。游戏中有需要多人进行配合的团队竞技，玩法基于一定难度的思维判断和肢体操作，鼓励玩家通过沟通、思考和训练达成游戏目标。
      游戏中存在基于文字交流的陌生人社交系统，但社交系统的管理遵循相关法律法规。</span><br /><br />
    <span class="agetxt">
      本游戏中有用户实名认证系统，认证为未成年人的用户将接受以下管理：</span><br /><br />
    <span class="agetxt">游戏中部分玩法和道具需要付费。未满8周岁的用户不能付费;
      8周岁以上未满16周岁的未成年人用户，单次充值金额不得超过50元人民币，每月充值金额累计不得超过200元人民币;
      16周岁以上的未成年人用户，单次充值金额不得超过100元人民币，每月充值金额累计不得超过400元人民币。</span><br /><br />
    <span class="agetxt">认证为未成年人的用户除周五、周六、周日及法定节假日每日20时至21时外其他时间均不可进入游戏。</span><br /><br />
    <span class="agetxt">本游戏以战舰的协同作战为主要游戏策略点，游戏竞技中的操作训练有助干锻炼玩家的逻辑思维能力，
      提高手眼协调能力和反应能力。部分基于团队开展的玩法，需要玩家共同努力、互相帮助来完成游戏任务，
      有助于玩家提升沟通能力、建立团队合作意识。军武颖材结合中华传统文化元素，有助于玩家开阔眼界、了解中华传统文化。</span><br /><br /><br />
  </el-dialog>
</template>

<script setup>
import { ref } from "vue";
import { ElMessage } from "element-plus";

let iconname = ref("战舰世界");
let icontxt = ref("云游戏");
const showwarning = ref(false);
const logintip = () => {
  ElMessage.error("请先登陆账号！");
};

</script>

<style lang="scss" scoped>
.agetxt {
  font-size: 20px;
}

.top {
  display: flex;
  padding-top: 60px;
  justify-content: space-between;

  .icon {
    display: inline-flex;
    font-size: 35px;
    align-items: center;
    justify-content: center;
    fill: currentColor;

    .iconleft {
      width: 40px;
      height: 35px;
      vertical-align: middle;
    }

    .icontxt {
      display: flex;
      align-items: center;
      font-size: 35px;
      background-image: linear-gradient(to right, #8effc6, #8eff8e, #ffff8e);
      background-clip: text;
      color: transparent;

      .iconright {
        width: 45px;
        height: 45px;
        vertical-align: middle;
      }
    }
  }

  .navs {
    display: flex;
    width: 700px;
    justify-content: space-between;
    align-items: center;

    .nav {
      display: flex;

      .navitemfirst {
        margin-left: 0;
        color: #25ffa9;
      }

      .navitem {
        &:hover {
          color: #25ffa9;
        }
      }
    }

    .login {
      display: flex;
      margin-left: 0;
      align-items: center;
      color: #fff;

      .loginpic {
        display: flex;
        width: 30px;
        height: 30px;
        margin-left: 20px;
      }

      .loginbtn {
        margin-left: 15px;
        opacity: 0.6;
        font-size: 14px;
        color: #fff;
        transition: opacity 0.5s;
        cursor: pointer;

        &:hover {
          opacity: 1;
        }
      }
    }
  }

  .agewarn {
    position: absolute;
    width: 50px;
    height: 60px;
    top: 750px;
    cursor: pointer;
  }
}

a {
  color: white;
  transition: color 0.5s;
  text-decoration: none;
}

li {
  position: relative;
  color: white;
  list-style: none;
  margin-left: 60px;
  font-size: 20px;
  transition: color 0.5s;
  font-weight: bold;
  cursor: pointer;

  &:hover {
    color: #25ffa9;
  }
}
</style>
