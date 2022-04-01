<template>
  <div>
    <div class="mt-2.5 mb-5">
      <lazy-image-loader
        paths="teams-page-images/team-leads.png"
        imageStyles=""
        containerStyles="flex justify-center items-center"
        alt=""
      ></lazy-image-loader>
    </div>
    <div>
      <p class="px-9 text-xs sm:text-base lg:text-xl leading-7">
        {{ firstParagraph }}
      </p>
    </div>
    <div class="team_leads flex justify-center mx-4 mt-32">
      <div
        class="team_leads_data flex flex-col items-center justify-start"
        v-for="(data, index) in leadData"
        :key="index"
      >
        <lazy-image-loader
          :paths="`teams-page-images/lead4.png`"
          imageStyles="w-20 h-20 sm:h-28 sm:w-28"
          containerStyles=" "
          alt=""
        ></lazy-image-loader>
        <p class="text-nexblack mt-4 text-xs">{{ data.name }}</p>
        <p class="text-nexblack mt-2 font-medium text-base text-nexred">
          {{ data.position }}
        </p>
        <div v-for="(socials, index) in data.socialMedia" :key="index">
          <p>{{ socials }}</p>
          <!-- <lazy-image-loader
        :paths="`footer-icons/social-media-icons/${socials}.png`"
        imageStyles=""
        containerStyles=""
        alt=""
      ></lazy-image-loader> -->
        </div>
      </div>
    </div>

    <div class="pt-8">
      <div
        class="partners flex flex-col justify-center items-center mt-14 mb-5"
      >
        <lazy-image-loader
          :paths="`teams-page-images/partners.png`"
          imageStyles=" "
          containerStyles="mb-5"
          alt="partners"
        ></lazy-image-loader>
        <p class="px-9 text-xs leading-7 pb-4">{{ secondParagraph }}</p>
      </div>

      <nuxt-link class="flex justify-center mb-6 sm:mb-12" to="/">
        <custom-button>Partner With Us</custom-button>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
import teamLeadParagraphs, {
  teamLeadData,
} from "../components/databases/teamsPage.js";
export default {
  data() {
    return {
      firstParagraph: teamLeadParagraphs[0],
      secondParagraph: teamLeadParagraphs[1],
      leadData: teamLeadData,
    };
  },
};
</script>

<style scoped>
@media (min-width: 0) {
  .team_leads {
    flex-wrap: wrap;
  }

  .team_leads_data {
    flex: 1 1 33.3%;
  }

  .text-nexblack {
    color: #202223;
  }

  .text-nexred {
    color: #fb3a3a;
  }
}

@media (min-width: 640px) {
  .team_leads_data {
    flex: 1 1 25%;
  }
}
</style>
