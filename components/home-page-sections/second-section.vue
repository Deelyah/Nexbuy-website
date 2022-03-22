<template>
  <section class="section_two w-full pt-10 lg:flex lg:justify-center">
    <div class="flex justify-center items-center">
      <img src="~/assets/mobile-mockup.png" alt="" />
    </div>
    <div
      class="flex flex-col lg:w-2/4 items-center justify-center px-10 lg:px-0"
    >
      <h2 class="text-lg font-semibold mb-2.5">
        Download now and shop with ease
      </h2>
      <p
        :class="`section_two_p${index + 1}`"
        v-for="(data, index) in dataForSectionTwo"
        :key="index"
      >
        {{ data }}
      </p>
      <!-- lg:ml-10 mobile-mockup flex justify-center bg-no-repeat mt-9 -->
      <!-- section_two_data_container flex flex-col justify-center items-center w-full lg:w-2/4 lg:mt-9 -->
      <div class="lg:flex">
        <div>
          <custom-button styling="lg:mr-20 mb-12">Download Now</custom-button>
        </div>
        <div>
          <custom-button styling="mb-18">Visit Web App</custom-button>
        </div>
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
@media (min-width: 0) {
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
    font-size: 12px;
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
}

@media (min-width: 640px) {
  .section_two_p2,
  .section_two_p3,
  .section_two_p4 {
    font-size: 18px;
  }
}
</style>
