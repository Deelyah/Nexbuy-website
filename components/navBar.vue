<template>
  <div class="w-full pl-3 pr-8 xl:pl-24 xl:pr-20 mt-0">
    <div class="flex justify-end">
      <nuxt-link class="mr-auto w-28 flex items-center" to="/home">
        <img
          class="object-cover h-20 w-full"
          src="../assets/logo.svg"
          alt="logo"
        />
      </nuxt-link>
      <div class="pt-5 pb-2.5">
        <div class="hidden xl:p-2.5">
          <nuxt-link class="xl:text-lg xl:mr-6 font-normal" to="/"
            >HOME</nuxt-link
          >
          <nuxt-link
            v-for="items in navOptions"
            :key="items"
            class="xl:text-lg xl:mr-6 font-normal"
            :to="items.toLowerCase()"
          >
            {{ items.toUpperCase() }}
          </nuxt-link>
        </div>
        <div class="p-2.5">
          <img src="~/assets/hamburger-menu.png" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      navOptions: ["About", "Team", "Services", "Blog", "Contact"],
    };
  },
};
</script>

<style scoped>
@media (min-width: 0px) {
  a {
    color: #202223;
  }

  .nuxt-link-exact-active {
    color: red;
  }
}

@media (min-width: 460px) {
}

@media (min-width: 640px) {
}

@media (min-width: 1024px) {
}

@media (min-width: 1280px) {
}
</style>
