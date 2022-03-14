<template>
  <div>
    <div
      v-for="(store, index) in downloadStores"
      :key="index"
      class="flex justify-end mt-1.5"
    >
      <button
        class="flex items-center pl-5 pr-3 py-2 mb-4 rounded"
        :class="setBackgroundColor"
      >
        <div>
          <img
            :src="
              require(`~/assets/footer-icons/${store}store${setIconColor}.png`)
            "
            :alt="`${store}store`"
            class="mr-5"
          />
        </div>
        <div>
          <p class="text-xs">Download on</p>
          <h4 class="text-lg">
            {{ store.replace(store[0], store[0].toUpperCase()) }} Store
          </h4>
        </div>
      </button>
    </div>
  </div>
</template>

<script>
import footerData from "./footer-details/footer-db";

export default {
  props: ["background", "extraStyling"],
  data() {
    return {
      downloadStores: footerData[5].downloadStores,
    };
  },
  computed: {
    setBackgroundColor() {
      if (this.background == "black") {
        return "dark";
      } else {
        return "light";
      }
    },

    setDisplay() {
      return `${this.extraStyling}`;
    },

    setIconColor() {
      if (this.background == "black") {
        return 1;
      } else {
        return 2;
      }
    },
  },
};
</script>

<style scoped>
.dark {
  background-color: #202223;
}

.light {
  background-color: #fff;
}
</style>
