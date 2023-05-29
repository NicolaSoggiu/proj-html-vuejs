<script>
import NavbarMenu from "./NavBarMenu.vue";
import NavbarSocial from "./NavbarSocial.vue";

export default {
  data() {
    return {
      arrNavbarMenu: [
        {
          voice: "Home",
        },
        {
          voice: "Blog",
        },
        {
          voice: "Pages",
        },
        {
          voice: "About",
        },
        {
          voice: "Contacts",
        },
        {
          voice: "Gallery",
        },
        {
          voice: "Shop",
        },
      ],
      arrIcons: [
        {
          icon: ["fas", "magnifying-glass"],
        },
        {
          icon: ["fab", "facebook-f"],
        },
        {
          icon: ["fab", "twitter"],
        },
        {
          icon: ["fab", "youtube"],
        },
        {
          icon: ["fab", "instagram"],
        },
      ],
    };
  },
  components: {
    NavbarMenu,
    NavbarSocial,
  },
};
</script>

<template>
  <header>
    <nav class="navbar">
      <div class="nav-logo">
        <img src="../../public/img/logo.svg" alt="" />
      </div>
      <div>
        <ul class="nav-menu">
          <NavbarMenu
            v-for="voices in arrNavbarMenu"
            :key="voices"
            :voices="voices"
          />
        </ul>
      </div>
      <div class="nav-social">
        <NavbarSocial
          v-for="socialMedia in arrIcons"
          :key="socialMedia"
          :socialMedia="socialMedia"
        />
      </div>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
// GENERAL

header {
  height: 10vh;

  // NAVBAR

  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem;
    .nav-logo {
      padding-left: 0.5rem;
      img {
        width: 150px;
      }
    }
    .nav-menu {
      display: flex;
      font-size: 0.8rem;
      gap: 1.5rem;
    }
    .nav-social {
      display: flex;
      gap: 1rem;
      padding-right: 1rem;
    }
  }
}
</style>
