<script>
export default {
  props: {
    card: Object,
    watch: Object,
  },
};
</script>

<template>
  <div class="card">
    <div class="img-container">
      <img :src="card.img" alt="" />
    </div>
    <h2>{{ card.title }}</h2>
    <span>{{ card.text }}</span>
  </div>
</template>

<style lang="scss" scoped>
.card {
  width: calc((100% / 3) - 2rem);
  display: flex;
  flex-direction: column;
  text-align: center;
  img {
    aspect-ratio: 1 / 1;
    width: 60px;
    padding-bottom: 1rem;
  }
  h2 {
    padding-bottom: 1rem;
    font-size: 1rem;
  }
  span {
    font-size: 0.6rem;
  }
}
</style>
