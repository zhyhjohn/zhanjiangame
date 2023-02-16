<template>
  <footer class="footer">
    <div class="container">
      <div class="logo">
        <span class="footer-logo">
          <img src="../assets/footerlogo1.png" alt="" />
        </span>
        <span class="footer-logo">
          <a href="https://p1.ssl.qhimg.com/d/inn/4be9e4098b53/txz.jpg">
            <img src="../assets/footerlogo2.png" alt="" /></a>
        </span>
      </div>
      <div class="footer-text">
        <p>© 2011 – 2020 Wargaming.net保留所有权利</p>
        <p>
          Copyright 2016 YouXi.com 版权所有 趣游时代(北京)科技有限公司
          北京市朝阳区酒仙桥路甲10号3号楼15层17层1769
        </p>
        <p><a href="https://s5.ssl.qhres2.com/static/b6e17859264cd813.pdf">京ICP证京B2-20170671</a> | 京ICP备11029981号-10 |
          <a href="https://p1.ssl.qhimg.com/d/inn/4be9e4098b53/txz.jpg">京网文【2019】0038-009号</a>
        </p>
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
  </footer>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.footer {
  width: 100%;
  padding-top: 20px;
  padding-bottom: 20px;
  background-color: #000;

  .container {
    position: relative;
    width: 100%;
    margin-right: auto;
    margin-left: auto;
    display: inline-flex;
    align-items: center;
    text-align: right;
    justify-content: center;

    .logo {
      .footer-logo {
        margin-right: 20px;
      }
    }

    .footer-text {
      display: inline-block;
      font-size: 12px;
      line-height: 20px;
      text-align: left;
      color: #9a9999;
      user-select:none;
    }
  }
}

p {
  margin: 0;
  padding: 0;
  list-style: none;
  box-sizing: border-box;
}
a {
  color: #9a9999;
  text-decoration: none;
}
</style>