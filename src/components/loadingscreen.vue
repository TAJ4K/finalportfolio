Stole this from here :D
https://dev.to/dd8888/how-to-create-a-simple-loading-screen-using-vue-4h7m

<template>
  <div
    class="absolute bg-cyan-700 h-full w-screen text-center z-[100] leading-[100vh]"
  >
    <img
      class="relative m-auto mt-[20%]"
      src="../../public/dialingprogress.gif"
      alt="loading..."
      width="250"
      v-if="isMobile"
    />
    <video
      autoplay
      loop
      muted
      playsinline
      src="@/../public/dialingprogress.webm"
      alt="loading..."
      class="relative m-auto mt-[20%]"
      width="250"
      v-else
    ></video>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "LoadingScreen",
  data() {
    return {
      isMobile: false,
    };
  },
  mounted() {
    this.isMobile = window.innerWidth < 768;
  },
});
</script>

<style>
#loading {
  position: absolute;
  z-index: 1000;
  background-color: rgb(107, 111, 199);
  height: 100vh;
  width: 100vw;
  text-align: center;
  line-height: 100vh;
}
.img {
  position: relative;
  margin: auto;
  margin-top: 20%;
}
</style>
