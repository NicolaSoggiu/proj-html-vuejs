<script>
export default {
  props: {
    voices: Object,
  },
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    toggleDropdown() {
      this.isOpen = !this.isOpen;
    },
  },
};
</script>

<template>
  <li>
    <a href="#" @click="toggleDropdown">{{ voices.voice }}</a>
    <ul v-if="isOpen" class="dropdown-menu">
      <li class="drop">SERVICES</li>
      <li class="drop">OUR WORK FLOW</li>
      <li class="drop">VIDEO THUMBNAIL TYPE</li>
    </ul>
  </li>
</template>

<style lang="scss" scoped>
li {
  list-style: none;
}

a {
  text-decoration: none;
  color: black;
}

.dropdown-menu {
  z-index: 4;
  position: fixed;
}

.drop {
  background-color: black;
  color: lightgrey;
  color: grey;
  padding: 1rem;
  border: 1px solid white;
  cursor: pointer;
  &:hover {
    color: white;
  }
}
</style>
