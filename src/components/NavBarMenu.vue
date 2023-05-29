<script>
export default {
  props: {
    voices: Object,
  },
};
</script>

<template>
  <li>
    <a href="#">
      {{ voices.voice }}
    </a>
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
</style>
