<template>
  <div>
    <button class="px-8 py-3 lg:px-10 lg:py-4 rounded-lg" :class="styling">
      <slot></slot>
    </button>
  </div>
</template>

<script>
export default {
  props: ["styling"],
};
</script>

<style scoped>
button {
  background-color: #fb3a3a;
  color: #fff;
}
</style>
