<template>
  <div>
    <div class="w-full pl-3 pr-8 xl:pl-24 xl:pr-20 mt-0">
      <!--#1 The div above contains all nav-elements including the hamburger menu which is displayed on tablets and phones -->
      <div class="flex justify-end">
        <nuxt-link class="mr-auto w-28 flex items-center" to="/">
          <!--#2 This is nexbuy logo. It is also a link to the homePage -->
          <img
            class="object-cover h-20 w-16 sm:w-full"
            src="../assets/logo.png"
            alt="logo"
          />
        </nuxt-link>

        <div class="pt-5 pb-2.5">
          <!--#3 All links are stored in an aray in the scripts to reduce HTML contents -->
          <div class="hidden lg:block p-2.5">
            <nuxt-link
              v-for="items in navOptions"
              :key="items"
              class="text-sm mr-6"
              :to="items == 'Home' ? '/' : items.toLowerCase()"
            >
              <!--#4 :to="items.toLowerCase() means that the route paths to each page are same as the name of the link in lower case" -->
              {{ items.toUpperCase() }}
            </nuxt-link>
          </div>
          <button @click="openDropdown" class="lg:hidden p-2.5">
            <img src="~/assets/hamburger-menu.png" alt="" />
          </button>
        </div>
      </div>
    </div>

    <div :class="`${sideMenu} fixed bg-white`">
      <button
        @click="closeDropdown"
        class="close_btn flex p-2 rounded-full ml-60 mr-4 mt-5"
      >
        <img src="~/assets/close.png" alt="" />
      </button>
      <ul>
        <li @click="closeDropdown" v-for="items in navOptions" :key="items">
          <nuxt-link
            class="block pl-6 py-4 font-semibold"
            :to="items == 'Home' ? '/' : items.toLowerCase()"
            >{{ items.toUpperCase() }}</nuxt-link
          >
        </li>
      </ul>
    </div>
  </div>
  <!-- </div> -->
</template>

<script>
export default {
  data() {
    return {
      navOptions: ["Home", "About", "Team", "Services", "Blog", "Contact"],
      sideMenu: "hidden",
    };
  },
  methods: {
    openDropdown() {
      this.sideMenu = "dropdown";
    },
    closeDropdown() {
      this.sideMenu = "hidden";
    },
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
    font-weight: bold;
  }

  li {
    cursor: pointer;
  }

  li:hover {
    background-color: #e7e7e7;
  }

  button {
    border: 0.5px solid transparent;
  }

  button:hover {
    background-color: #f1f1f1;
    border: 0.5px solid #e7e7e7;
    border-radius: 4px;
  }

  button img {
    min-width: 11px;
  }

  .dropdown {
    top: -384px;
    right: -296px;
    animation: open-menu 0.4s 1;
    animation-timing-function: ease-in-out;
    animation-fill-mode: forwards;
  }

  @keyframes open-menu {
    from {
      top: -384px;
      right: -296px;
    }
    to {
      top: 0;
      right: 0;
    }
  }
}
</style>
