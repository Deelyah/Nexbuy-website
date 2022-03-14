<!--eslint-disable -->
<template>
  <div class="flex flex-col text-white fixed left-0 right-0 bottom-0">
    <div class="upper-footer-section pt-16 pl-7 pr-24">
      <div class="flex ml-24 mr-2">
        <div class="w-full">
          <div v-for="(data, index) in footerData[0].tel" :key="index">
            <p>
              Tel ({{ index + 1 }}):
              <a href="#"> {{ data }}</a>
            </p>
          </div>
          <div class="my-5">
            <p>
              Email:
              <a
                v-for="(data, index) in footerData[1].mails"
                :key="index"
                :href="`mailto:${data}`"
              >
                {{ data }} <br
              /></a>
            </p>
          </div>
          <div>
            <p>
              Lagos, Nigeria 100001 <br />
              Lake City Plaza, Gudu District, FCT, Nigeria 902101
            </p>
          </div>
        </div>
        <div class="flex flex-col w-full">
          <nuxt-link
            v-for="(data, index) in footerData[2].links"
            :key="index"
            :to="`/${data.toLowerCase()}`"
            class="mb-2.5"
            >{{ data }}</nuxt-link
          >
        </div>
        <div class="flex flex-col w-full">
          <nuxt-link
            v-for="(data, index) in footerData[3].products"
            :key="index"
            :to="`/${data.toLowerCase()}`"
            class="mb-2.5"
            >{{ data }}</nuxt-link
          >
          <nuxt-link to="/" class="mt-4">Careers at Nexbuy</nuxt-link>
        </div>
        <div class="w-full">
          <div class="flex items-center justify-center mb-14">
            <a
              v-for="(icon, index) in iconName"
              :key="index"
              class="ml-3.5 w-full"
              href="#"
            >
              <img
                :src="require(`~/assets/${icon.toLowerCase()}.png`)"
                :alt="icon"
                :title="icon"
              />
            </a>
          </div>
          <div
            v-for="(store, index) in downloadStores"
            :key="index"
            class="flex justify-end mt-1.5"
          >
            <button class="flex items-center pl-5 pr-3 py-2 mb-4 rounded">
              <div>
                <img
                  :src="require(`~/assets/${store}store.png`)"
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
      </div>
    </div>
    <div class="lower-footer-section text-center w-full">
      <p class="py-5 text-white text-base font-light">
        All rights reserved. Nexbuy District LLC, {{ new Date().getFullYear() }}
      </p>
    </div>
  </div>
</template>

<script>
import footerData from "./footer-db";
export default {
  data() {
    return {
      footerData: [...footerData],
      iconName: footerData[4].social[0].socialMediaIcons,
      downloadStores: footerData[5].downloadStores,
    };
  },

  mounted() {
    console.log(this.iconName);
  },
};
</script>

<style scoped>
.upper-footer-section {
  background-color: #333;
}
.lower-footer-section,
button {
  background-color: #202223;
}
</style>
