<template>
  <section class="flex justify-center">
    <div class="w-[40rem] min-w-[20rem] h-[15rem] bg-yellow-400 relative">
      <div class="flex flex-row flex-wrap justify-between h-6 px-1">
        <div><strong>GruxLP</strong></div>
        <div>2022</div>
      </div>
      <hr class="border-black" />
      <div class="px-1 flex flex-col justify-between h-[13.5rem]">
        <p>
          Project compilation website for a local real estate company. (Work In
          Progress)
        </p>
        <div class="flex flex-col mx-5">
          <a href="https://gruxlp.com" class="underline" target="_blank">
            Website Link
          </a>
        </div>
        <p>Built with: Vue, MongoDB</p>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "GruxProject",
});
</script>
