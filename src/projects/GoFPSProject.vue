<template>
  <section
    class="grow min-w-[20rem] md:min-w-[19rem] md:max-w-[19rem] h-[15rem] md:h-[24rem] bg-yellow-400"
  >
    <div class="flex flex-row justify-between h-6 px-1">
      <div><strong>Go FPS</strong></div>
      <div>2022</div>
    </div>
    <hr class="border-black" />
    <div class="px-1 flex flex-col justify-between h-[13.5rem] md:h-[22.5rem]">
      <p>
        Wrapper/API for
        <a href="https://fastpeoplesearch.com/">fastpeoplesearch</a>, allowing
        for easy access to their database of people. Main applications would be
        fraud/risk detection.
      </p>
      <div class="flex flex-col mx-5">
        <a
          href="https://pkg.go.dev/github.com/TAJ4K/gofps"
          class="underline"
          target="_blank"
        >
          pkg.go.dev
        </a>
        <a
          href="https://github.com/taj4k/gofps"
          class="underline"
          target="_blank"
        >
          Github Repo
        </a>
      </div>
      <p>Built with: Go</p>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "PkgProject",
});
</script>
