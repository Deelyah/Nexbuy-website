<template>
  <div>
    <button class="px-10 py-4 rounded-lg" :class="styling">
      <slot></slot>
    </button>
  </div>
</template>

<script>
export default {
  props: ['styling'],
};
</script>

<style scoped>
button{
  background-color: #FB3A3A;
  color: #fff;
}
</style>></style>
