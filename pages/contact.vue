<template>
  <div class="flex flex-col justify-center items-center">
    <h2>Contact Us</h2>
    <Form class="px-6">
      <legend class="text-center">Message us</legend>
      <input class="w-full py-3 pl-2 mb-4" type="text" placeholder="Name" />
      <input
        class="w-full py-3 pl-2 mb-4"
        type="text"
        placeholder="Email Address"
      />
      <textarea
        class="w-full"
        name=""
        id=""
        cols="30"
        rows="10"
        placeholder="Message"
      ></textarea>
    </Form>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
form {
  border: 0.3px solid #fb3a3a;
  width: 331px;
  height: 390px;
}

input,
textarea {
  border: 0.3px solid #ff73654d;
  background-color: #f8f8f8;
}
</style>
