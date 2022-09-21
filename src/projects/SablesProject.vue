<template>
  <section class="flex justify-center">
    <div class="w-[40rem] min-w-[20rem] h-[15rem] bg-yellow-400 relative">
      <div class="flex flex-row flex-wrap justify-between h-12 sm:h-6 px-1">
        <div><strong>Sables</strong>, a tool for the visually impaired</div>
        <div>2022</div>
      </div>
      <hr class="border-black" />
      <div class="px-1 flex flex-col justify-between h-[12rem] sm:h-[13.5rem]">
        <p>
          Client-side tool that uses Amazon's Rekognition API to help identify
          blurry images for those who struggle with their vision online.
        </p>
        <div class="flex flex-col mx-5">
          <a href="https://sables.tech" class="underline" target="_blank">
            Website Link
          </a>
          <a
            href="https://github.com/taj4k/sables"
            class="underline"
            target="_blank"
          >
            Github Repo
          </a>
        </div>
        <p>Built with: Go, AWS, Vue</p>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "SablesProject",
});
</script>
