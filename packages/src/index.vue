<template>
  <div class="spinners">
    <div ref="facebook" :class="cStyle">
      <div ref="first"></div>
      <div ref="second"></div>
      <div ref="third"></div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Spinners",
  props: {
    type: {
      type: String,
      default: "small",
    },
  },
  computed: {
    cStyle() {
      switch (this.type) {
        case "small":
          return "small";
          break;
        case "middle":
          return "middle";
          break;
        default:
          return "default";
      }
    },
  },
};
</script>
<style lang="less" scoped>
.spinners {
  width: 80px;
  height: 80px;
  .default {
    display: inline-block;
    position: relative;
    width: 80px;
    height: 80px;
  }
  .default div {
    display: inline-block;
    position: absolute;
    left: 8px;
    width: 16px;
    background: #fff;
    animation: default 1.2s cubic-bezier(0, 0.5, 0.5, 1) infinite;
  }

  .default div:nth-child(1) {
    left: 8px;
    animation-delay: -0.24s;
  }
  .default div:nth-child(2) {
    left: 32px;
    animation-delay: -0.12s;
  }
  .default div:nth-child(3) {
    left: 56px;
    animation-delay: 0;
  }

  @keyframes default {
    0% {
      top: 8px;
      height: 64px;
    }
    50%,
    100% {
      top: 24px;
      height: 32px;
    }
  }

  .small {
    display: inline-block;
    position: relative;
    width: 40px;
    height: 40px;
  }

  .small div {
    display: inline-block;
    position: absolute;
    left: 4px;
    width: 8px;
    background: #fff;
    animation: small 1.2s cubic-bezier(0, 0.5, 0.5, 1) infinite;
  }

  .small div:nth-child(1) {
    left: 4px;
    animation-delay: -0.24s;
  }
  .small div:nth-child(2) {
    left: 16px;
    animation-delay: -0.12s;
  }
  .small div:nth-child(3) {
    left: 28px;
    animation-delay: 0;
  }

  @keyframes small {
    0% {
      top: 4px;
      height: 32px;
    }
    50%,
    100% {
      top: 12px;
      height: 16px;
    }
  }

  .middle {
    display: inline-block;
    position: relative;
    width: 50px;
    height: 50px;
  }

  .middle div {
    display: inline-block;
    position: absolute;
    left: 6px;
    width: 10px;
    background: #fff;
    animation: middle 1.2s cubic-bezier(0, 0.5, 0.5, 1) infinite;
  }

  .middle div:nth-child(1) {
    left: 6px;
    animation-delay: -0.24s;
  }
  .middle div:nth-child(2) {
    left: 18px;
    animation-delay: -0.12s;
  }
  .middle div:nth-child(3) {
    left: 30px;
    animation-delay: 0;
  }

  @keyframes middle {
    0% {
      top: 4px;
      height: 34px;
    }
    50%,
    100% {
      top: 12px;
      height: 18px;
    }
  }
}
</style>