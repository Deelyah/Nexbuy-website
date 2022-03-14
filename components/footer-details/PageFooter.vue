<template>
  <div class="flex flex-col text-white">
    <section class="upper-footer-section pt-16 pl-7 pr-24">
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
                :src="
                  require(`~/assets/footer-icons/social-media-icons/${icon.toLowerCase()}.png`)
                "
                :alt="icon"
                :title="icon"
              />
            </a>
          </div>
          <app-download background="black" />
        </div>
      </div>
    </section>
    <section class="lower-footer-section text-center w-full">
      <p class="py-5 text-white text-base font-light">
        All rights reserved. Nexbuy District LLC, {{ new Date().getFullYear() }}
      </p>
    </section>
  </div>
</template>

<script>
import AppDownload from "../DownloadButton.vue";
import footerData from "./footer-db";
export default {
  components: { AppDownload },
  data() {
    return {
      footerData: [...footerData],
      iconName: footerData[4].social[0].socialMediaIcons,
      downloadStores: footerData[5].downloadStores,
    };
  },
};
</script>

<style scoped>
.upper-footer-section {
  background-color: #333;
}
.lower-footer-section {
  background-color: #202223;
}
</style>
