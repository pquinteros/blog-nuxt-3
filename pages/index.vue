<template>
  <div>
    <div class="static" :class="{ active: isActive, 'text-danger': hasError }">index</div>
    <div :class="classObject"></div>
  </div>
</template>
<script setup>
const isActive = ref(true)
const hasError = ref(false)
const classObject = reactive({
  active: true,
  'text-danger': false
})
const color = '#ffcc00';
</script>
<style lang="scss">
.active {
  font-weight: bold;
  color: v-bind(color);
}
</style>