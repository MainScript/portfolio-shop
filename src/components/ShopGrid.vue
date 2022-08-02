<template>
  <div class="outer-grid">
    <div class="grid">
      <div class="grid-item" v-for="item in items" :key="item.title">
        <BasicCard>
          <template #header>
            <h1>{{ item.title }}</h1>
          </template>
          <p>{{ item.description }}</p>
        </BasicCard>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import BasicCard from "@/components/shared/BasicCard.vue";
import { Item } from "@/models";

export default defineComponent({
  name: "ShopGrid",
  components: {
    BasicCard,
  },
  props: {
    items: {
      type: Array as () => Item[],
      required: true,
    },
  },
});
</script>
<style lang="scss" scoped>
.outer-grid {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  height: 100%;
  .grid {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    width: 90%;
    .grid-item {
      width: calc(33% - 1rem);
      margin: 0.5rem;
    }
  }
}
</style>
