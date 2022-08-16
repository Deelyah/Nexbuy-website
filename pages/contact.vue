<template>
  <div class="flex flex-col justify-center items-center">
    <h2 class="text-2xl font-semibold mb-12 sm:text-4xl">Contact Us</h2>
    <Form class="px-6 pt-5 mb-36 sm:mb-56">
      <legend class="text-center mb-6 text-xl font-semibold">Message us</legend>
      <input
        class="w-full py-3 pl-2 mb-4 sm:py-5 sm:pl-4 rounded"
        type="text"
        placeholder="Name"
      />
      <input
        class="w-full py-3 pl-2 mb-4 sm:py-5 sm:pl-4 rounded"
        type="text"
        placeholder="Email Address"
      />
      <textarea
        class="w-full py-3 pl-4 rounded"
        name=""
        id=""
        cols="30"
        rows="10"
        placeholder="Message"
      ></textarea>
      <div class="flex justify-center mt-11 mb-6 sm:mb-12">
        <nuxt-link to="/">
          <custom-button>Send</custom-button>
        </nuxt-link>
      </div>
    </Form>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
@media (min-width: 0) {
  h2 {
    color: #fb3a3a;
  }

  form {
    border: 0.3px solid rgba(255, 115, 101, 0.5);
    width: 331px;
    height: auto;
  }

  input,
  textarea {
    border: 0.3px solid #ff73654d;
    background-color: #f8f8f8;
  }

  input:focus,
  textarea:focus {
    border: 0.3px solid #ff73654d;
    outline: transparent;
  }
}

@media (min-width: 640px) {
  form {
    width: 550px;
    height: auto;
  }
}
</style>
