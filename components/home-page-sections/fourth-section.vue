<template>
  <section class="section_four pt-52 pb-32">
    <div class="flex justify-center items-center mb-14">
      <div class="circle one flex flex-col items-center py-14">
        <div class="w-12 h-12 mb-6">
          <img src="~/assets/mission.png" alt="Our mission" />
        </div>
        <div>
          <h2 class="mb-6 font-semibold text-3xl">Our Mission</h2>
        </div>
        <div>
          <p class="ml-8 mr-10 text-center text-xl">
            Offering trust in mediation and providing the right number of
            prospects.
          </p>
        </div>
      </div>
      <div class="bg-link">
        <img width="298px" height="115px" src="~/assets/bg-link.png" alt="" />
      </div>
      <div class="circle two flex flex-col items-center py-14">
        <div class="h-12 w-12 mb-6">
          <img src="~/assets/vision.png" alt="" />
        </div>
        <div>
          <h2 class="mb-6 font-semibold text-3xl">Our Vision</h2>
        </div>
        <div>
          <p class="text-xl mx-16 text-center">
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
.section_four {
  background-color: #e5e5e5;
}

.circle {
  background-color: #fff;
  width: 327px;
  height: 327px;
  border-radius: 50%;
}

.one {
  margin-right: -85px;
  z-index: 5;
}

.two {
  margin-left: -110px;
  z-index: 5;
}
</style>
