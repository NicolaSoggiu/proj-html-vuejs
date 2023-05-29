<script>
export default {
  props: {
    card: Object,
  },
};
</script>

<template>
  <div class="card">
    <img :src="card.img" alt="" />
    <h2>{{ card.title }}</h2>
    <span>{{ card.text }}</span>
  </div>
</template>

<style lang="scss" scoped></style>
