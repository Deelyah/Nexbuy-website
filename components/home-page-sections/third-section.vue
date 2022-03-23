<template>
  <div class="py-14">
    <div class="px-4 flex justify-end md:pl-0 items-center">
      <div class="testimonials flex flex-col md:w-2/4">
        <div class="flex justify-center mb-5">
          <img
            src="~/assets/opening-quote.png"
            class="opening_quote mr-auto"
            alt="opening-quote"
          />
          <img
            class="closing_quote ml-auto"
            src="~/assets/closing-quote.png"
            alt="closing-quote"
          />
        </div>
        <div class="flex justify-center items-center">
          <p class="px-5 lg:px-0 text-center sm:text-lg md:flex md:flex-col">
            <span>I like that Nexbuy is very easy and swift to use.</span>
            <span>
              I have different sales made quickly with this app. Really
              transformational.</span
            >
          </p>
        </div>
      </div>
      <div class="w-1/4">
        <div class="flex justify-center lg:justify-end">
          <img src="~/assets/arrow-right.png" alt="arrow" />
        </div>
      </div>
    </div>
    <div class="flex justify-center items-center mt-7">
      <div class="mr-5">
        <img src="~/assets/passport.png" alt="passport" />
      </div>
      <div>
        <p class="text-sm font-normal">Amaka Chisom</p>
        <p class="text-sm font-light">Fashion Entrepreneur</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
@media (min-width: 0px) {
  .opening_quote,
  .closing_quote {
    width: 22px;
    height: 17px;
  }
}

@media (min-width: 640px) {
  .opening_quote,
  .closing_quote {
    width: 35px;
    height: 27px;
  }
}

@media (min-width: 1024px) {
  .opening_quote,
  .closing_quote {
    width: 50px;
    height: 40px;
  }
}
</style>
