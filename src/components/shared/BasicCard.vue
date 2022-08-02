<template>
  <div class="card">
    <div class="card-header">
      <slot name="header"></slot>
    </div>
    <div class="card-body">
      <slot></slot>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "BasicCard",
});
</script>
<style lang="scss" scoped>
.card {
  background-color: $card-bg-light;
  padding: $card-padding;
  border-radius: $card-border-radius;
  box-shadow: $card-box-shadow;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  height: 100%;
  transition: all 0.3s ease-in-out;
  &:hover {
    color: $card-hover-light;
    cursor: pointer;
  }
}
</style>
