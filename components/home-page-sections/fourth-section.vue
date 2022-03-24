<template>
  <section class="section_four pt-52 pb-32">
    <div class="flex flex-col justify-center items-center lg:mb-14">
      <div class="circle one flex flex-col items-center lg:py-14">
        <div class="w-12 h-12 lg:mb-6 my-4 lg:my-0">
          <img src="~/assets/mission.png" alt="Our mission" />
        </div>
        <div>
          <h2 class="mb-3 lg:mb-6 font-semibold text-3xl">Our Mission</h2>
        </div>
        <div>
          <p class="ml-8 mr-10 text-center text-base lg:text-xl">
            Offering trust in mediation and providing the right number of
            prospects.
          </p>
        </div>
      </div>
      <div class="bg-link">
        <img width="298px" height="115px" src="~/assets/bg-link.png" alt="" />
      </div>
      <div
        class="circle two flex flex-col justify-center items-center lg:py-14"
      >
        <div class="h-12 w-12 lg:mb-6">
          <img src="~/assets/vision.png" alt="" />
        </div>
        <div>
          <h2 class="mb-3 lg:mb-6 font-semibold text-3xl">Our Vision</h2>
        </div>
        <div>
          <p class="text-base lg:text-xl px-10 lg:px-16 text-center">
            A whole new-tech transactional world.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
@media (min-width: 0) {
  .section_four {
    background-color: #e5e5e5;
  }

  .circle {
    background-color: #fff;
    width: 250px;
    height: 250px;
    border-radius: 50%;
  }

  .one {
    z-index: 5;
    margin-bottom: -10px;
  }

  .two {
    z-index: 5;
    margin-top: -20px;
  }

  .bg-link > img {
    transform: rotate(84deg);
    margin-right: 30px;
  }
}

@media (min-width: 640px) {
  .one {
    margin-bottom: -10px;
  }

  .two {
    margin-top: -40px;
  }
}

@media (min-width: 1024px) {
  .section_four > div {
    flex-direction: row;
  }

  .circle {
    width: 327px;
    height: 327px;
  }
  .one {
    margin-right: -85px;

    /* z-index: 5; */
  }

  .two {
    margin-left: -110px;
    /* z-index: 5; */
  }

  .bg-link > img {
    transform: rotate(0deg);
  }
}
</style>
