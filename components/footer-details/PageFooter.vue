<!--eslint-disable -->
<template>
  <div class="flex flex-col text-white fixed left-0 right-0 bottom-0">
    <div class="flex bg-black upper-footer-section pt-16 ml-2 pl-24">
      <div>
        <div v-for="(data, index) in footerData[0].tel" :key="index">
          <p>
            Tel ({{ index + 1 }}):
            <a href="#"> {{ data }}</a>
          </p>
        </div>
        <div>
          <p>
            Email
            <a
              v-for="(data, index) in footerData[1].mails"
              :key="index"
              :href="`mailto:${data}`"
              >{{ data }} <br
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
      <div class="flex flex-col">
        <nuxt-link
          v-for="(data, index) in footerData[2].links"
          :key="index"
          :to="`/${data.toLowerCase()}`"
          >{{ data }}</nuxt-link
        >
      </div>
      <div class="flex flex-col">
        <nuxt-link
          v-for="(data, index) in footerData[3].products"
          :key="index"
          :to="`/${data.toLowerCase()}`"
          >{{ data }}</nuxt-link
        >
        <nuxt-link to="">Careers at Nexbuy</nuxt-link>
      </div>
      <div>
        <div class="flex items-center">
          <a v-for="(icon, index) in iconName" :key="index" class="mr-3.5">
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
          class="flex items-center"
        >
          <div>
            <img
              :src="require(`~/assets/${store}store.png`)"
              :alt="`${store}store`"
            />
          </div>
          <div>
            <p>Download on</p>
            <h4>{{ store.replace(store[0], store[0].toUpperCase()) }} Store</h4>
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
.lower-footer-section {
  background-color: #202223;
}
</style>
