<script>
export default {
  props: {
    socialMedia: Object,
  },
};
</script>

<template>
  <a href="#">
    <font-awesome-icon :icon="socialMedia.icon" />
  </a>
</template>

<style lang="scss" scoped>
a {
  text-decoration: none;
  color: black;
}
</style>
