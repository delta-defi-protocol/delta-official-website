<template>
  <div class="first-banner" id="firstScreen">
    <div class="global-width">
      <app-header-PC/>
      <app-header-Mobile/>
      <div class="main flex">
        <span class="animatin-icon icon-rectangle02 hide-mobile">
          <img :src="rectangle02" alt="rectangle">
        </span>
        <div class="first-banner-left col-md-6 col-sm-12">
          <span class="animatin-icon icon-polygonIcon02 hide-mobile">
            <img :src="polygonIcon02" alt="tusd">
          </span>
          <h2>{{$t('home.maintitle01')}}</h2>
          <h2>{{$t('home.maintitle02')}}</h2>
          <p>{{$t('home.text01')}}</p>
          <p>{{$t('home.text02')}}</p>
          <p class="btn-wrap">
            <a
              class="btn-white"
              target="_blank"
              href="https://app.bretton.finance/home"
            >{{$t('home.useApp')}}</a>
            <a class="btn-primary">{{$t('home.preview')}}</a>
          </p>

          <span class="animatin-icon icon-polygonIcon03 hide-mobile">
            <img :src="polygonIcon03" alt="tusd">
          </span>
          <span class="animatin-icon icon-ovalIcon01 hide-mobile">
            <img :src="ovalIcon01" alt="tusd">
          </span>
        </div>
        <div class="first-banner-right col-md-6 col-sm-12">
          <span class="animatin-icon icon-ovalIcon02 hide-mobile">
            <img :src="ovalIcon01" alt="tusd">
          </span>
          <div class="icon-box-wrap">
            <div class="icon-box">
              <div class="delta">
                <!-- <img :src="deltaIcon" alt="delta"> -->
              </div>
              <span class="icon-tsud">
                <img :src="tusdIcon" alt="tusd">
              </span>
              <span class="icon-usdt">
                <img :src="usdtIcon" alt="usdt">
              </span>
              <span class="icon-usdc">
                <img :src="usdcIcon" alt="usdc">
              </span>
              <span class="icon-dai">
                <img :src="daiIcon" alt="dai">
              </span>
            </div>
            <span class="animatin-icon icon-oval02 hide-mobile">
              <img :src="ovalIcon02" alt="ovalIcon02">
            </span>
            <span class="animatin-icon icon-rectangle hide-mobile">
              <img :src="rectangleIcon01" alt="rectangleIcon01">
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AppHeaderPC from "@/components/AppHeaderPC.vue";
import AppHeaderMobile from "@/components/AppHeaderMobile.vue";
export default {
  name: "FirstScreen",

  components: {
    AppHeaderPC,
    AppHeaderMobile
  },

  data() {
    return {
      msg: "first screen",
      deltaIcon: require("@/assets/images/firstBanner/icon-delta.png"),
      tusdIcon: require("@/assets/images/firstBanner/icon-tusd.png"),
      usdtIcon: require("@/assets/images/firstBanner/icon-usdt.png"),
      usdcIcon: require("@/assets/images/firstBanner/icon-usdc.png"),
      daiIcon: require("@/assets/images/firstBanner/icon-dai.png"),
      ovalIcon01: require("@/assets/images/firstBanner/icon-oval01.png"),
      ovalIcon02: require("@/assets/images/firstBanner/icon-oval02.png"),
      ovalIcon03: require("@/assets/images/firstBanner/icon-oval03.png"),
      polygonIcon01: require("@/assets/images/firstBanner/icon-polygon01.png"),
      polygonIcon02: require("@/assets/images/firstBanner/icon-polygon02.png"),
      polygonIcon03: require("@/assets/images/firstBanner/icon-polygon03.png"),
      rectangleIcon01: require("@/assets/images/firstBanner/icon-rectangle01.png"),
      rectangle02: require("@/assets/images/firstBanner/icon-rectangle02.png")
    };
  },

  computed: {
    // isMobile: {}
  }
};
</script>

<style scoped lang="scss">
.main {
  padding: 3%;
}
.first-banner {
  background: linear-gradient(
    360deg,
    rgba(255, 119, 84, 1) 0%,
    rgba(253, 38, 124, 1) 100%
  );
  height: 100%;
  width: 100%;

  &-left {
    padding-top: 0.8rem;
    padding-left: 0.4rem;
    position: relative;

    > h2 {
      font-size: 72px;
      font-weight: bold;
      line-height: 88px;
      color: rgba(255, 255, 255, 1);
      opacity: 1;
      text-align: left;
    }

    > p {
      font-size: 16px;
      font-weight: 400;
      line-height: 32px;
      color: rgba(255, 255, 255, 0.6);
      text-align: left;

      &:nth-of-type(1) {
        margin-top: 0.4rem;
      }
      &.btn-wrap {
        margin-top: 0.6rem;
        margin-bottom: 0.6rem;
      }
      .btn-white,
      .btn-primary {
        background: rgba(255, 255, 255, 1);
        border-radius: 0.2rem;
        font-size: 14px;
        font-weight: 400;
        line-height: 24px;
        color: rgba(253, 38, 124, 1);
        opacity: 1;
        padding: 10px 32px;
        cursor: pointer;
        display: initial;
      }

      .btn-primary {
        border: solid 1px white;
        background: transparent;
        color: white;
        margin-left: 24px;
      }
    }
  }

  &-right {
    position: relative;
    margin-top: 1.2rem;
    .icon-box-wrap {
      max-width: 80%;
    }
    .icon-box {
      position: relative;
      display: inline-block;
      background-image: url("../assets/images/firstBanner/icon-delta.png");
      background-size: contain;
      background-repeat: no-repeat;
      width: 4rem;
      height: 4rem;
      max-width: 100%;

      > span {
        position: absolute;
        z-index: 1;
        width: 1.2rem;
        height: 1.2rem;

        img {
          max-width: 100%;
        }

        &:nth-of-type(1) {
          top: -0.16rem;
          right: 0.6rem;
        }
        &:nth-of-type(2) {
          top: 0.4rem;
          right: -1.2rem;
        }
        &:nth-of-type(3) {
          bottom: 0.2rem;
          right: 0.3rem;
        }
        &:nth-of-type(4) {
          bottom: 0.14rem;
          left: 0.2rem;
        }
      }
    }
  }

  .animatin-icon {
    position: absolute;
    display: inline-block;
    width: 46px;
    height: 52px;
    img {
      max-width: 100%;
    }

    &.icon-rectangle {
      width: 0.93rem;
      height: 0.93rem;
      right: 0.84rem;
      bottom: -1.2rem;
      z-index: 0;
    }

    &.icon-rectangle02 {
      width: 1.2rem;
      height: 1.2rem;
      left: -0.6px;
      top: 3.38rem;
      z-index: 0;
    }

    &.icon-oval02 {
      top: 52%;
      right: -18%;
    }

    &.icon-oval01 {
      top: -0.85rem;
      right: 0.58rem;
    }

    &.icon-ovalIcon01 {
      left: 2.1rem;
      bottom: 1.42rem;
    }

    &.icon-ovalIcon02 {
      left: 3.9rem;
      top: -1.1rem;
    }

    &.icon-polygonIcon02 {
      top: 0.43rem;
      left: -0.39rem;
    }
    &.icon-polygonIcon03 {
      left: -0.18rem;
      bottom: 0.33rem;
    }
  }
}
@media (max-width: 768px) {
  .main {
    padding-top: 0;
  }
  .first-banner {
    height: auto;

    .app-header-pc {
      display: none;
    }

    .app-header-mobile {
      display: flex;
    }

    &-left {
      order: 2;
      padding-top: 0.4rem;

      > p {
        text-align: center;
        .btn-wrap {
          margin-top: 0.3rem;
          margin-bottom: 0.3rem;
        }

        &:nth-of-type(1) {
          margin-top: 0.3rem;
        }
      }

      > h2 {
        font-size: 56px;
        text-align: center;
      }
    }

    &-right {
      order: 1;
      margin-top: 0.3rem;

      .icon-box {
        width: 2.5rem;
        height: 2.5rem;
      }

      .icon-box-wrap {
        margin: 0 auto;
      }

      .icon-box > span {
        width: 0.8rem;
        height: 0.8rem;

        &:nth-of-type(1) {
          top: -0.04rem;
          right: 0.3rem;
        }
        &:nth-of-type(2) {
          top: 0.4rem;
          right: -0.6rem;
        }
        &:nth-of-type(3) {
          bottom: 0.2rem;
          right: 0.1rem;
        }
        &:nth-of-type(4) {
          bottom: 0.07rem;
          left: 0.2rem;
        }
      }
    }
  }
}
</style>
<style lang="scss">
.icon-ovalIcon01 {
  animation: move01 3s infinite;
}
@keyframes move01 {
  0% {
    bottom: 1.42rem;
  }
  50% {
    bottom: 1.26rem;
  }
  100% {
    bottom: 1.42rem;
  }
}
.icon-polygonIcon02 {
  animation: move02 3s infinite;
}
@keyframes move02 {
  0% {
    top: 0.43rem;
  }
  50% {
    top: 0.59rem;
  }
  100% {
    top: 0.43rem;
  }
}
.icon-polygonIcon03 {
  animation: move03 3s infinite;
}
@keyframes move03 {
  0% {
    bottom: 0.33rem;
  }
  50% {
    bottom: 0.16rem;
  }
  100% {
    bottom: 0.33rem;
  }
}
.icon-ovalIcon02 {
  animation: move04 2s infinite;
}
@keyframes move04 {
  0% {
    top: -1.1rem;
  }
  50% {
    top: -1rem;
  }
  100% {
    top: -1.1rem;
  }
}
.icon-rectangle {
  animation: move05 2s infinite;
}
@keyframes move05 {
  0% {
    bottom: -1.2rem;
  }
  50% {
    bottom: -1.4rem;
  }
  100% {
    bottom: -1.2rem;
  }
}
.icon-tsud {
  animation: move06 2s infinite;
}
@keyframes move06 {
  0% {
    top: -0.16rem;
  }
  50% {
    top: -0.06rem;
  }
  100% {
    top: -0.16rem;
  }
}
.icon-usdt {
  animation: move07 2s infinite;
}
@keyframes move07 {
  0% {
    top: 0.4rem;
  }
  50% {
    top: 0.3rem;
  }
  100% {
    top: 0.4rem;
  }
}
.icon-usdc {
  animation: move08 4s infinite;
}
@keyframes move08 {
  0% {
    bottom: 0.2rem;
  }
  50% {
    bottom: 0.1rem;
  }
  100% {
    bottom: 0.2rem;
  }
}
.icon-dai {
  animation: move09 2s infinite;
}
@keyframes move09 {
  0% {
    bottom: 0.14rem;
  }
  50% {
    bottom: 0.06rem;
  }
  100% {
    bottom: 0.14rem;
  }
}
.icon-oval02 {
  animation: move010 2s infinite;
}
@keyframes move010 {
  0% {
    top: 52%;
  }
  50% {
    top: 46%;
  }
  100% {
    top: 52%;
  }
}
.icon-rectangle02 {
  animation: move011 2s infinite;
}
@keyframes move011 {
  0% {
    top: 3.38rem;
  }
  50% {
    top: 3.28rem;
  }
  100% {
    top: 3.38rem;
  }
}
</style>

