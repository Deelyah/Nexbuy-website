<template>
  <div class="w-full">
    <div
      class="image bg-cover bg-no-repeat flex flex-col justify-center text-white items-center"
    >
      <div class="px-3">
        <h2
          class="text-lg sm:text-2xl lg:text-3xl xl:text-4xl text-center font-semibold"
        >
          THE BEST E-COMMERCE SOLUTION YOUR BUSINESS NEEDS
        </h2>
      </div>
      <div>
        <p class="text-sm sm:text-lg lg:text-2xl text-center mt-5 mb-6">
          Your business is more than a business, it is our Priority.
        </p>
      </div>
      <div class="lg:mt-28 flex justify-center items-center">
        <download-button
          background="light"
          display="lg:flex"
          extraStyling="text-black lg:mx-8"
        />
      </div>
    </div>

    <section class="section_one pt-16 md:pt-72 pb-2 lg:pb-64">
      <div>
        <div
          v-for="(items, index) in homeDatabase"
          :key="index"
          class="lg:flex lg:justify-center mb-36"
        >
          <lazy-image-loader
            :paths="`${items.image}.png`"
            imageStyles="lg:mr-32 mb-6 lg:mb-0"
            containerStyles="flex justify-center lg:justify-end items-center"
          ></lazy-image-loader>
          <div
            class="lg:w-2/4 lg:flex lg:flex-col lg:items-center justify-center"
          >
            <h2
              class="font-semibold text-center mb-5 md:mb-8 text-red-600 text-4xl"
            >
              {{ items.title }}
            </h2>
            <p
              :class="`section_one_data${
                index + 1
              } px-9 md:px-20 lg:px-0 text-sm md:text-xl lg:text-lg  leading-7`"
            >
              {{ items.description }}
            </p>
          </div>
        </div>
      </div>
    </section>

    <second-section />
    <third-section />

    <fourth-section />

    <!-- <fifth-section />-->
    <sixth-section />
  </div>
</template>

<script>
// import CustomButton from "../components/CustomButton.vue";
import dataForSectionOne from "../components/databases/homePage-db";
import SecondSection from "../components/home-page-sections/second-section.vue";
import ThirdSection from "../components/home-page-sections/third-section.vue";
import FourthSection from "../components/home-page-sections/fourth-section.vue";
// import FifthSection from "../components/home-page-sections/fifth-section.vue";
import SixthSection from "../components/home-page-sections/sixth-section.vue";

export default {
  components: {
    //CustomButton,
    SecondSection,
    ThirdSection,
    FourthSection,
    // FifthSection,
    SixthSection,
  },
  name: "IndexPage",
  data() {
    return {
      homeDatabase: dataForSectionOne,
    };
  },
};
</script>

<style>
@import url(https://fonts.googleapis.com/css2?family=Lato:wght@100;200;300;400;500;600;800;900&display=swap);

@media (min-width: 0) {
  body {
    font-family: "Lato";
  }
  .section_one {
    background: #e5e5e5;
  }
  .image {
    height: 430px;
    background-image: url("~assets/home_image2.png");
  }
}

@media (min-width: 460px) {
  .image {
    height: 600px;
  }
}

@media (min-width: 640px) {
  .image {
    height: 550px;
    background-image: url("~assets/home_image.png");
  }
}

@media (min-width: 1024px) {
  .image {
    height: 600px;
  }

  .section_one_data2 {
    padding-left: 40px;
    padding-right: 0;
  }
}

@media (min-width: 1280px) {
}
</style>
