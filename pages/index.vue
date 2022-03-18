<template>
  <div>
    <!-- <div
      class="image bg-cover bg-no-repeat w-full flex flex-col justify-center text-white items-center"
    >
      <h2 class="text-4xl font-semibold">
        THE BEST E-COMMERCE SOLUTION YOUR BUSINESS NEEDS
      </h2>
      <p class="text-2xl mt-5">
        Your business is more than a business, it is our Priority.
      </p>
      <div class="mt-28 flex justify-center items-center">
        <download-button
          background="light"
          display="flex"
          extraStyling="text-black mx-8"
        />
      </div>
    </div>

    <section class="section_one pt-72 pb-64">
      <div class="px-32">
        <div
          v-for="(items, index) in homeDatabase"
          :key="index"
          class="flex justify-center items-center mb-36"
        >
          <img class="mr-32" :src="require(`~/assets/${items.image}.png`)" />
          <div>
            <h2 class="font-semibold text-center mb-8 text-red-600 text-4xl">
              {{ items.title }}
            </h2>
            <p :class="`section_one_data${index + 1} text-2xl`">
              {{ items.description }}
            </p>
          </div>
        </div>
      </div> 
    </section>-->
    <!-- <second-section />
    <third-section />
    <fourth-section />
    <fifth-section />
    <sixth-section /> -->
  </div>
</template>

<script>
// import CustomButton from "../components/CustomButton.vue";
// import dataForSectionOne from "../components/databases/homePage-db";
// import SecondSection from "../components/home-page-sections/second-section.vue";
// import ThirdSection from "../components/home-page-sections/third-section.vue";
// import FourthSection from "../components/home-page-sections/fourth-section.vue";
// import FifthSection from "../components/home-page-sections/fifth-section.vue";
// import SixthSection from "../components/home-page-sections/sixth-section.vue";

// export default {
//   components: {
//     CustomButton,
//     SecondSection,
//     ThirdSection,
//     FourthSection,
//     FifthSection,
//     SixthSection,
//   },
//   name: "IndexPage",
//   data() {
//     return {
//       homeDatabase: dataForSectionOne,
//     };
//   },
// };
</script>

<style>
/* @import url(https://fonts.googleapis.com/css2?family=Lato:wght@100;200;300;400;500;600;800;900&display=swap);

body {
  font-family: "Lato";
}

.section_one {
  background: #e5e5e5;
}
.image {
  background-image: url("~assets/home_image.png");
  height: 700px;
}

.section_one_data2 {
  padding-left: 80px;
} */
</style>
