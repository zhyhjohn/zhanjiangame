<template>
  <div class="footer">
    <div class="logo">
      <img src="../assets/footerlogo.png" alt="" />
    </div>
    <div class="text">
      <p>© 2011 – 2020 Wargaming.net保留所有权利</p>
      <p>
        Copyright 2016 YouXi.com 版权所有 趣游时代(北京)科技有限公司
        北京市朝阳区酒仙桥路甲10号3号楼15层17层1769
      </p>
      <p>京ICP证京B2-20170671 京ICP证京B2-20170671 京ICP证京B2-20170671</p>
      <p>
        公安备案号11010502035516 | ISBN-978-7-89989-132-2 |
        新出审字【2011】186号
      </p>
      <p>
        抵制不良游戏 拒绝盗版游戏 注意自我保护 谨防受骗上当 适度游戏益脑
        沉迷游戏伤身 合理安排时间 享受健康生活
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "MyFooter",
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.footer {
  width: 100%;
  height: 150px;
  background-color: #000000;
  margin-top: 610px;
  .logo {
    width: 250px;
    height: 70px;
    padding-top: 40px;
    margin-left: 400px;
    float: left;
  }
  .text {
    margin: {
      top: 20px;
      right: 100px;
    }
    width: 700px;
    height: 70px;
    font-size: 3px;
    color: white;
    float: right;
  }
}
</style>