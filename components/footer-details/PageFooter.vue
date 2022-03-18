<template>
  <div class="flex flex-col text-white">
    <section class="upper-footer-section pb-7">
      <div
        class="pt-8 px-9 text-sm lg:text-base lg:pt-16 lg:px-10 lg:flex lg:flex-row-reverse"
      >
        <div class="w-full mb-7">
          <div class="flex items-center justify-center lg:justify-end lg:mb-16">
            <!-- This div contains the social media icons. -->
            <!-- Social media icons are fetched from footer-db.js in the script -->
            <a
              v-for="(icon, index) in iconName"
              :key="index"
              class="ml-3.5"
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
          <download-button
            class="hidden lg:block"
            display="block"
            background="black"
          />
          <!-- download-button contains the button to download from app and play store -->
          <!-- "background" refers to the backgroundColor of the entire button -->
        </div>
        <div class="flex lg:w-full">
          <div class="flex flex-col w-full lg:ml-6">
            <!-- this lists home, about, FAQs, Teams, services etc which is fetched from footer-db.js in the script -->

            <nuxt-link
              v-for="(data, index) in footerData[2].links"
              :key="index"
              :to="`/${data.toLowerCase()}`"
              class="mb-2.5"
              >{{ data }}</nuxt-link
            >
          </div>
          <div class="flex flex-col w-full">
            <!--this lists nexbuy, nexscrow, nexcoin etc which is stored in homePage-db.js -->

            <nuxt-link
              v-for="(data, index) in footerData[3].products"
              :key="index"
              :to="`/${data.toLowerCase()}`"
              class="mb-2.5"
              >{{ data }}</nuxt-link
            >
            <nuxt-link to="/" class="mt-4">Careers at Nexbuy</nuxt-link>
          </div>
        </div>
        <div class="sm:flex lg:w-full">
          <download-button
            class="flex justify-start mt-10 sm:w-full lg:hidden"
            background="black"
          />
          <div class="w-full sm:ml-auto">
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
import DownloadButton from "../DownloadButton.vue";
import footerData from "../databases/footer-db";
export default {
  components: { DownloadButton },
  data() {
    return {
      footerData: [...footerData], //returns an array containing all items stored for the footer
      iconName: footerData[4].social[0].socialMediaIcons, //returns all social media icons for this page
      downloadStores: footerData[5].downloadStores, //returns download buttons
    };
  },
};
</script>

<style scoped>
.upper-footer-section {
  background-color: #333;
}
img {
  min-width: 20px;
  min-height: 20px;
}
.lower-footer-section {
  background-color: #202223;
}
</style>
