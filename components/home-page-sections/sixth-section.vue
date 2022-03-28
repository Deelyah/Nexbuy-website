<template>
  <div class="mt-10">
    <div class="flex flex-col justify-center pt-9 px-8 items-center">
      <h2 class="mb-5 text-xl sm:text-2xl lg:text-4xl font-semibold">
        Subscribe to our newsletter
      </h2>
      <p class="mb-16 text-xs sm:text-base md:text-lg lg:text-xl">
        Exciting deals are always available! Be the first to know
      </p>
      <form
        class="w-full flex justify-center lg:pt-11 mb-44 pb-3 sm:px-11 md:px-20"
      >
        <div class="input_div w-2/4 pl-6 lg:pt-2 lg:pb-2">
          <input class="py-2" type="email" placeholder="Enter email address" />
        </div>
        <button
          class="text-white lg:text-2xl font-medium px-6 py-3 lg:pt-0 lg:pb-0"
        >
          Subscribe
        </button>
      </form>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
h2 {
  color: #fb3a3a;
}

button {
  background-color: #fb3a3a;
}

input {
  outline: none;
  /* width: 269px; */
}

.input_div {
  border: 1px solid #fb3a3a;
}
</style>
