<template>
  <div class="pl-24 pr-20 mt-0">
    <div class="flex justify-end">
      <nuxt-link class="mr-auto w-28 flex items-center" to="/home">
        <img
          class="object-cover h-20 w-full"
          src="../assets/logo.svg"
          alt="logo"
        />
      </nuxt-link>
      <div class="pt-5 pb-2.5">
        <div class="p-2.5">
          <nuxt-link class="text-lg mr-6 last:mr-0 font-normal" to="/"
            >HOME</nuxt-link
          >
          <nuxt-link
            v-for="items in navOptions"
            :key="items"
            class="text-lg mr-6 last:mr-0 font-normal"
            :to="items.toLowerCase()"
          >
            {{ items.toUpperCase() }}
          </nuxt-link>
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
