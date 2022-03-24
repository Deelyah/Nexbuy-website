<template>
  <div>
    <section
      class="section_one bg-e5e5e5 flex justify-center items-center pt-3 pb-11"
    >
      <h2 class="font-semibold text-3xl">About Our Application</h2>
    </section>
    <section class="section_two bg-e5e5e5">
      <div class="about_us"></div>
      <div class="flex flex-col items-center justify-center pt-8 lg:pt-24 px-8">
        <h2 class="text-lg sm:text-2xl lg:text-3xl mb-3 font-semibold">
          Innovative E-commerce for all
        </h2>
        <p class="p1 text-left text-xs sm:text-base sm:px-20 font-normal">
          {{ firstParagraph }}
        </p>
      </div>

      <div
        class="mt-20 md:flex justify-center items-center px-8 pb-20 lg:pb-32"
      >
        <img
          class="story max-w-md mb-8 mx-auto md:w-full"
          src="~assets/about-page-images/section-two.png"
          alt=""
        />

        <div class="flex flex-col justify-center items-center md:pl-8 lg:w-3/4">
          <h2 class="text-lg sm:text-2xl lg:text-3xl font-semibold mb-3">
            Our Story
          </h2>
          <p class="text-xs sm:pl-8 flex flex-col">
            <span class="mb-8 sm:text-lg lg:leading-10">{{
              secondParagraph
            }}</span
            ><span class="mb-40 md:mb-0 sm:text-lg lg:leading-10">{{
              thirdParagraph
            }}</span>
          </p>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import aboutPageDatabase from "../components/databases/aboutPage-bd";
export default {
  data() {
    return {
      firstParagraph: aboutPageDatabase[0],
      secondParagraph: aboutPageDatabase[1],
      thirdParagraph: aboutPageDatabase[2],
    };
  },
};
</script>

<style scoped>
@media (min-width: 0) {
  .bg-e5e5e5 {
    background-color: #e5e5e5;
  }

  .about_us {
    height: 83px;
    width: 100%;
    background-repeat: no-repeat;
    background-size: cover;
    background-image: url("~assets/about-page-images/about_us.png");
  }

  h2 {
    color: #fb3a3a;
    border-bottom: 2px solid #fb3a3a;
  }
  p {
    line-height: 28px;
  }

  .story {
    max-height: 600px;
  }
}

@media (min-width: 350px) {
  .about_us {
    height: 100px;
  }
}

@media (min-width: 500px) {
  .about_us {
    height: 120px;
  }
}

@media (min-width: 600px) {
  .about_us {
    height: 150px;
  }
}

@media (min-width: 768px) {
  .about_us {
    height: 200px;
  }
}

@media (min-width: 800px) {
  .about_us {
    background-image: url("~assets/about-page-images/about_us2.png");
    height: 250px;
  }
}

@media (min-width: 1024px) {
  .about_us {
    height: 350px;
  }
}
</style>
