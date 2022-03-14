<template>
  <div>
    <div class="image flex flex-col justify-center text-white items-center">
      <h2 class="text-4xl">THE BEST E-COMMERCE SOLUTION YOUR BUSINESS NEEDS</h2>
      <p class="text-2xl mt-5">
        Your business is more than a business, it is our Priority.
      </p>
      <div>
        <download-button background="light" extraStyling="text-black mr-5" />
      </div>
    </div>

    <div></div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>

<style>
@import url(https://fonts.googleapis.com/css2?family=Lato:wght@100;200;300;400;500;600;800;900&display=swap);

body {
  font-family: "Lato", sans-serif;
}

.image {
  background-image: url("~assets/home_image.png");
  height: 650px;
  width: 100%;
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
