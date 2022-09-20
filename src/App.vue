<template>
  <div :class="{ 'mx-16': !isLoading }">
    <img
      src="../public/wordart.png"
      alt="Kobe Rankich"
      class="block ml-auto mr-auto py-4 w-96 h-auto"
      :class="{ hidden: isLoading }"
    />
    <LoadingScreen v-if="isLoading"></LoadingScreen>
    <div v-else id="content">
      <MeBox />
      <div class="spacer"></div>
      <SablesProject />
      <div class="spacer"></div>
      <div class="flex justify-center">
        <div class="flex justify-center flew-row gap-8 flex-wrap w-[40rem]">
          <PkgProject />
          <GoFPSProject />
        </div>
      </div>
      <div class="spacer"></div>
      <img
        id="ie"
        src="../public/best_viewed_with.jpg"
        class="fixed h-24 bottom-0 left-0"
        v-if="!isLoading && !tooSmall"
      />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import MeBox from "./components/mebox.vue";
import LoadingScreen from "./components/loadingscreen.vue";

import SablesProject from "./projects/SablesProject.vue";
import PkgProject from "./projects/PkgProject.vue";
import GoFPSProject from "./projects/GoFPSProject.vue";

export default defineComponent({
  name: "App",
  components: {
    MeBox,
    LoadingScreen,
    SablesProject,
    PkgProject,
    GoFPSProject,
  },
  data() {
    return {
      isLoading: true,
      tooSmall: false,
    };
  },
  mounted() {
    setTimeout(() => {
      this.isLoading = false;
    }, 2000);
    if (window.innerWidth < 945) {
      this.tooSmall = true;
    }
    window.onresize = () => {
      this.tooSmall = window.innerWidth < 945;
    };
    let title = document.title + "    ";
    setInterval(() => {
      title = title.substring(1, title.length) + title.substring(0, 1);
      document.title = title;
    }, 300);
  },
});
</script>
