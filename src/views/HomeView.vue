<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <ShopGrid :items="items" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ShopGrid from "@/components/ShopGrid.vue";
import { Item } from "../models";

export default defineComponent({
  name: "HomeView",
  components: {
    ShopGrid,
  },
  // create an array of items to display in the grid
  mounted() {
    this.items = [
      {
        title: "Vue.js",
        description: "The progressive JavaScript framework",
      },
      {
        title: "Vuex",
        description: "A state management solution for Vue.js",
      },
      {
        title: "Vue Router",
        description: "A routing framework for Vue.js",
      },
      {
        title: "Vue.js",
        description: "The progressive JavaScript framework",
      },
      {
        title: "Vuex",
        description: "A state management solution for Vue.js",
      },
      {
        title: "Vue Router",
        description: "A routing framework for Vue.js",
      },
      {
        title: "Vue.js",
        description: "The progressive JavaScript framework",
      },
      {
        title: "Vuex",
        description: "A state management solution for Vue.js",
      },
      {
        title: "Vue Router",
        description: "A routing framework for Vue.js",
      },
    ];
  },
  data() {
    return {
      items: [] as Item[],
    };
  },
});
</script>
