<template>
  <section class="section_two pt-10 flex">
    <div class="ml-10 mobile-mockup bg-no-repeat mt-9">
      <img src="~/assets/mobile-mockup.png" alt="" />
    </div>
    <div
      class="section_two_data_container flex flex-col justify-center items-center w-2/4 mt-9"
    >
      <h2 class="font-semibold mb-2.5">Download now and shop with ease</h2>
      <p
        :class="`section_two_p${index + 1}`"
        v-for="(data, index) in dataForSectionTwo"
        :key="index"
      >
        {{ data }}
      </p>
      <div class="flex">
        <custom-button styling="mr-20">Download Now</custom-button>
        <custom-button>Visit Web App</custom-button>
      </div>
    </div>
  </section>
</template>

<script>
import { dataForSectionTwo } from "../databases/homePage-db";
export default {
  data() {
    return {
      dataForSectionTwo: dataForSectionTwo,
    };
  },
};
</script>

<style>
.section_two {
  background-color: rgba(255, 115, 101, 0.05);
}

.mobile-mockup {
  height: 700px;
  width: 700px;
}

.section_two_data_container {
  background-color: rgba(255, 255, 255, 0);
}

.section_two_data_container h2 {
  font-size: 40px;
  color: #202223;
}

.section_two_p1 {
  color: #202223;
  text-align: center;
  font-size: 22px;
  padding: 0;
  margin-bottom: 50px;
}

.section_two_p2,
.section_two_p3,
.section_two_p4 {
  width: fit-content;
  color: #fb3a3a;
  font-size: 18px;
  padding: 15px 34px;
  margin-bottom: 45px;
  background-color: #fff;
  border-radius: 20px;
}

.section_two_p2 {
  margin-left: 20%;
}

.section_two_p3 {
  margin-right: auto;
}

.section_two_p4 {
  margin-left: auto;
  margin-bottom: 103px;
}
</style>
