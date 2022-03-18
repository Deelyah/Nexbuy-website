<template>
  <div class="section_five">
    <div class="flex flex-col justify-center items-center pt-12">
      <h2 class="font-semibold text-4xl mb-5">Latest on our blog</h2>
      <p class="text 2xl">
        Read our articles and blog posts. Never miss out on the latest gist.
      </p>
    </div>
    <div class="mx-20 mt-14">
      <div class="flex items-center justify-between px-11">
        <div class="mr-16 img_container">
          <img src="~/assets/three-in-one.png" alt="" />
        </div>
        <div>
          <h3>Join the next big thing at Nexbuy!</h3>
          <p>{{ sectionFiveData }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { dataForSectionFive } from "../databases/homePage-db";
export default {
  data() {
    return {
      sectionFiveData: dataForSectionFive,
    };
  },
};
</script>

<style scoped>
.section_five {
  background-color: rgba(255, 115, 101, 0.05);
}
</style>
