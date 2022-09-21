<template>
  <section
    class="grow min-w-[20rem] md:min-w-[19rem] md:max-w-[19rem] h-[15rem] md:h-[24rem] bg-yellow-400"
  >
    <div class="flex flex-row justify-between h-6 px-1">
      <div><strong>PKG File Resolver</strong></div>
      <div>2022</div>
    </div>
    <hr class="border-black" />
    <div class="px-1 flex flex-col justify-between h-[13.5rem] md:h-[22.5rem]">
      <p>
        Open source library on NPM that fixes an issue created by vercel/pkg's
        file system, where local directory references don't work between dev and
        prod.
      </p>
      <div class="flex flex-col mx-5">
        <a
          href="https://www.npmjs.com/package/pkg-file-resolver"
          class="underline"
          target="_blank"
        >
          NPM Page
        </a>
        <a
          href="https://github.com/taj4k/pkg-file-resolver"
          class="underline"
          target="_blank"
        >
          Github Repo
        </a>
      </div>
      <p>Built with: Node.js</p>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "PkgProject",
});
</script>
