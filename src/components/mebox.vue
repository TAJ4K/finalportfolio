<template>
  <div class="flex justify-center">
    <div class="text-center w-[40rem] min-w-[20rem] h-[14rem] bg-yellow-400">
      <div id="header" class="justify-between flex relative bg-orange-600">
        <div class="w-1/3"></div>
        <div class="w-1/3">ME :)))</div>
        <div class="w-1/3 text-right">{{ time }}</div>
      </div>
      <div id="meBody" class="flex px-4">
        <div
          id="links"
          class="w-1/2 h-[12.5rem] flex items-center justify-center"
        >
          <div class="grid grid-rows-2 grid-cols-2 gap-4 text-blue-800">
            <a target="_blank" href="https://github.com/taj4k">>>github</a>
            <a href="mailto:kobet12345@gmail.com">>>email</a>
            <a target="_blank" href="https://linkedin.com/in/jolt">
              >>linkedin
            </a>
            <a href="tel:+14255011802">>>phone</a>
          </div>
        </div>
        <div id="what" class="w-1/2 h-[12.5rem] flex justify-center">
          <img
            src="../../public/ComputerSpin.gif"
            alt="a laptop spinning"
            class="h-full"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "MeBox",
  data() {
    return {
      time: "",
    };
  },
  mounted() {
    setInterval(() => {
      this.time = new Date().toLocaleTimeString();
    }, 1000);
  },
});
</script>
