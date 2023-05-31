<script>
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
          isOpen: false,
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
  methods: {
    toggleDropdown(voice) {
      if (voice.voice === "Pages") {
        voice.isOpen = !voice.isOpen;
      }
    },
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
          <li
            v-for="voice in arrNavbarMenu"
            :key="voice.voice"
            :class="{ active: voice.isOpen }"
          >
            <a href="#" @click="toggleDropdown(voice)">
              {{ voice.voice }}
            </a>
            <ul v-if="voice.isOpen" class="dropdown-menu">
              <!-- Contenuto del dropdown menu -->
              <li class="drop">SERVICES</li>
              <li class="drop">OUR WORK FLOW</li>
              <li class="drop">VIDEO THUMBNAIL TYPE</li>
            </ul>
          </li>
        </ul>
      </div>
      <div class="nav-social">
        <a href="#" v-for="socialMedia in arrIcons" :key="socialMedia">
          <font-awesome-icon :icon="socialMedia.icon" />
        </a>
      </div>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
// GENERAL

a {
  text-decoration: none;
  color: black;
}

li {
  list-style: none;
}

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
.dropdown-menu {
  position: fixed;
  margin-top: 1.5rem;
  .drop {
    background-color: black;
    color: lightgrey;
    padding: 1rem;
    border: 1px solid white;
    cursor: pointer;
    &:hover {
      color: white;
    }
  }
}
</style>
