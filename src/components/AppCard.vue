<script>
export default {
  props: {
    data: Object,
    imgClass: String,
  },
};
</script>

<template>
  <div>
    <img :class="imgClass" :src="data.img" alt="" />
    <h2>{{ data.title }}</h2>
    <span>{{ data.text }}</span>
  </div>
</template>

<style lang="scss" scoped></style>
