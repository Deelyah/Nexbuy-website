<template>
  <div class="mt-10">
    <div class="flex flex-col justify-center pt-9 items-center">
      <h2 class="mb-5">Subscribe to our newsletter</h2>
      <p class="mb-16">
        Exciting deals are always available! Be the first to know
      </p>
      <form class="flex pt-11 mb-44 pb-3">
        <div class="input_div w-full pl-6 pt-4 pb-3 pr-72">
          <input class="py-2" type="email" placeholder="Enter email address" />
        </div>
        <button class="text-white font-medium px-6 pt-6 pb-5">Subscribe</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
h2 {
  font-size: 34px;
  font-weight: 600;
  color: #fb3a3a;
}

button {
  background-color: #fb3a3a;
  font-size: 26px;
}

input {
  outline: none;
  width: 269px;
}

.input_div {
  border: 1px solid #fb3a3a;
}
</style>
