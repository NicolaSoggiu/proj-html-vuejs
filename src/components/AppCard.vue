<script>
export default {
  props: {
    data: Object,
  },
};
</script>

<template>
  <div class="card">
    <div class="img-container">
      <img :src="data.img" alt="" />
    </div>
    <h2>{{ data.title }}</h2>
    <span>{{ data.text }}</span>
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
