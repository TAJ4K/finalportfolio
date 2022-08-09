<template>
  <div class="" :class="{ 'mx-16': !isLoading }">
    <LoadingScreen v-if="isLoading"></LoadingScreen>
    <img
      src="../public/wordart.png"
      alt="Kobe Rankich"
      class="block ml-auto mr-auto py-8 w-96 h-auto"
    />
    <MeBox />
    <img
      src="../public/best_viewed_with.jpg"
      class="absolute h-16 bottom-0 left-0"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import MeBox from "./components/mebox.vue";
import LoadingScreen from "./components/loadingscreen.vue";

export default defineComponent({
  name: "App",
  components: {
    MeBox,
    LoadingScreen,
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
