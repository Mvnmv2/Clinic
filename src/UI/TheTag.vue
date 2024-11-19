<script setup>

defineProps({
  heroBlock: Boolean
})

</script>

<template>
  <div class="tag heroBlock">
    <slot></slot>
  </div>
</template>

<style scoped lang="scss">
@import "@/assets/scss/variables.scss";

.tag {
  position: relative;
  top: -8px;
  left: 2px;

  width: 32px;
  height: 20px;
  border-radius: 24px;
  color: $white;
  font-weight: 500;
  font-size: 11px;
  background-color: $primary-color;

  display: flex;
  align-items: center;
  justify-content: center;
}

.heroBlock {
  position: absolute;
  top: -12%;
  left: 100%;
  transform: translateX(-100%);
}

</style>