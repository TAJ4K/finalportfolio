<template>
  <div class="flex justify-center">
    <div class="text-center w-[40rem] min-w-[20rem] h-[15rem] bg-yellow-400">
      <div id="header" class="justify-between flex relative bg-orange-600 px-1">
        <div class="w-1/3 text-left">{{ time }}</div>
        <div class="w-1/3">ME :)))</div>
        <div class="w-1/3 text-right">You are visitor #{{ count }}</div>
      </div>
      <div id="meBody" class="flex px-4">
        <div class="absolute text-xs"><i>Not a designer</i></div>
        <div
          id="links"
          class="w-1/2 h-[13.5rem] flex items-center justify-center"
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
        <div class="w-1/2 h-[13.5rem] flex justify-center items-center">
          <img
            src="@/../public/computer.png"
            alt="gif of a computer"
            class="h-32 sm:h-48"
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
      count: 0,
    };
  },
  mounted() {
    this.time = new Date().toLocaleTimeString();
    setInterval(() => {
      this.time = new Date().toLocaleTimeString();
    }, 1000);
    fetch("https://gentle-castle-49906.herokuapp.com/query")
      .then((res) => res.json())
      .then((data) => {
        this.count = data.count;
      });
  },
});
</script>
