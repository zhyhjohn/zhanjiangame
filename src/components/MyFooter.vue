<template>
  <Footer class="footer">
    <div class="container">
      <div class="logo">
        <span class="footerlogo">
          <img src="../assets/footerlogo.png" alt="" />
        </span>
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
  </Footer>
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
  padding: 20px 0;
  background-color: #000000;
  .container {
    position: relative;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    margin-right: auto;
    margin-left: auto;
    width: 100%;
    text-align: right;
    .logo {
      .footerlogo {
        margin-right: 20px;
      }
    }
    .text {
      display: inline-block;
      font-size: 12px;
      line-height: 20px;
      text-align: left;
      color: #9a9999;
    }
  }
}

p {
  margin: 0;
  padding: 0;
  list-style: none;
  box-sizing: border-box;
}
</style>