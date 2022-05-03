<template>
  <div class="wrapper">
    <video loop autoplay muted>
      <source type="video/mp4" src="../assets/finvid.mp4" />
    </video>
    <div
      @click="scrollToBenefits()"
      class="video-text d-flex flex-column align-center justify-center"
    >
      <div class="video-title text-center" style="">Био-фарма</div>
      <div class="video-subtitle text-center" style="color: green">
        <span
          class="px-1 mr-1"
          style="
            color: white;
            background-color: green;
            width: fit-content;
            font-weight: 100;
          "
        >
          Доверяя</span
        >
        научному подходу
      </div>
    </div>
  </div>
</template>

<script>
import { eventBus } from "../main";
export default {
  data() {
    return {};
  },
  methods: {
    scrollToBenefits() {
      eventBus.$emit("scroll-to-element", { component: "benefits" });
    },
  },
};
</script>

<style scoped>
.wrapper {
  background: white;
  overflow: hidden;
  position: relative;
  width: 100vw;
  height: 100vh;
}
.video-title {
  font-size: 80px;
  font-weight: 100;
  color: white;
}
.video-subtitle {
  font-size: 32px;
  font-weight: 300;
  margin-top: -25px;
  color: white;
}
.animate__animated.animate__shakeY {
  --animate-duration: 5000ms;
}
.video-text {
  z-index: 3;
  position: absolute;
  top: 50%;
  left: 0;
  width: 100%;
  -webkit-transform: translateY(-50%);
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
  cursor: pointer;
}
.advice {
  position: absolute;
  left: 50%;
  bottom: 50px;
  -webkit-transform: translateX(-50%);
  -ms-transform: translateX(-50%);
  transform: translateX(-50%);
}
video {
  filter: brightness(0.7);
  opacity: 0.5;
  position: absolute;
  top: 50%;
  left: 50%;
  min-width: 110%;
  min-height: 110%;
  width: auto;
  height: auto;
  -webkit-transform: translateX(-50%) translateY(-50%);
  -ms-transform: translateX(-50%) translateY(-50%);
  transform: translateX(-50%) translateY(-50%);
}
@media (max-width: 500px) {
  .video-title {
    font-size: 60px;
    font-weight: 100;
    color: white;
  }
  .video-subtitle {
    font-size: 22px;
    font-weight: 300;
    margin-top: -15px;
    color: white;
  }
}
</style>