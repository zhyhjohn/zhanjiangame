<template>
  <div class="layer"></div>
  <div class="container" ref="ScaleBox" :style="{
    width: width + 'px',
    height: height + 'px',
  }">
    <MyCover />
    <div class="main">
      <div class="content">
        <MyHeader />
        <MyPage />
      </div>
      <MyFooter />
    </div>
  </div>
</template>

<script>
import MyCover from './components/MyCover';
import MyHeader from './components/MyHeader';
import MyPage from './components/MyPage';
import MyFooter from './components/MyFooter';

export default {
  name: "App",
  components: { MyCover, MyHeader, MyPage, MyFooter },
  data() {
    return {
      scale: 0,
      width: 1920,
      height: 1080,
    };
  },
  mounted() {
    this.setScale();
    window.addEventListener("resize", this.debounce(this.setScale));
  },
  methods: {
    getScale() {
      // 固定好16：9的宽高比，计算出最合适的缩放比
      const { width, height } = this;
      const wh = window.innerHeight / height;
      const ww = window.innerWidth / width;
      console.log(ww < wh ? ww : wh);
      return ww < wh ? ww : wh;
    },
    setScale() {
      // 获取到缩放比例，设置它
      this.scale = this.getScale();
      if (this.$refs.ScaleBox) {
        this.$refs.ScaleBox.style.setProperty("--scale", this.scale);
      }
    },
    debounce(fn, delay) {
      const delays = delay || 500;
      let timer;
      return function () {
        const th = this;
        const args = arguments;
        if (timer) {
          clearTimeout(timer);
        }
        timer = setTimeout(function () {
          timer = null;
          fn.apply(th, args);
        }, delays);
      };
    },
  },
};
</script>

<style lang="scss" scoped>
#ScaleBox {
  --scale: 1;
}

.layer {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: #000;
  opacity: 1;
}

.container {
  position: absolute;
  display: flex;
  flex-direction: column;
  transform: scale(var(--scale)) translate(-50%, -50%);
  transform-origin: 0 0;
  left: 50%;
  top: 50%;
  transition: 0.3s;
  z-index: 999;

  .main {
    position: relative;
    width: 100%;
    height: 100%;

    .content {
      position: relative;
      margin: 0 280px 0 150px;
      height: 1080px;
      z-index: 99;
      overflow: hidden;
    }
  }
}

#app {
  height: 100%;
}
</style>
