<template>
  <div :class="`${containerStyles}`">
    <img
      :title="title"
      :src="require(`~/assets/${paths}`)"
      :alt="alt"
      :class="`${imageStyles}`"
    />
  </div>
</template>

<script>
export default {
  props: ["paths", "alt", "containerStyles", "imageStyles", "title"],
};
</script>

<style scoped>
@media (min-width: 0) {
  .story {
    max-height: 600px;
  }
}
</style>
