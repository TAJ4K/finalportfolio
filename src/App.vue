<template>
  <div :class="{ 'mx-16': !isLoading }">
    <LoadingScreen v-if="isLoading"></LoadingScreen>
    <div v-else id="content">
      <img
        src="../public/wordart.png"
        alt="Kobe Rankich"
        class="block ml-auto mr-auto pt-4 w-96 h-auto"
      />
      <MeBox />
      <SablesProject />
      <SablesProject />
      <SablesProject />
      <img
        id="ie"
        src="../public/best_viewed_with.jpg"
        class="fixed h-[10%] bottom-0 left-0 z-[1000]"
        v-if="!isLoading"
      />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import MeBox from "./components/mebox.vue";
import LoadingScreen from "./components/loadingscreen.vue";

import SablesProject from "./projects/SablesProject.vue";

export default defineComponent({
  name: "App",
  components: {
    MeBox,
    LoadingScreen,
    SablesProject,
  },
  data() {
    return {
      isLoading: true,
    };
  },
  mounted() {
    setTimeout(() => {
      this.isLoading = false;
    }, 2000);
  },
});
</script>
