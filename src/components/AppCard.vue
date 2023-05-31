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

<style lang="scss" scoped>
.imgclass1 {
  padding-bottom: 1rem;
  width: 320px;
}

.imgclass2 {
  padding-bottom: 1rem;
  width: 250px;
}

.imgclass3 {
  padding-bottom: 1rem;
  width: 60px;
}

span {
  color: grey;
  margin-top: 1rem;
}
</style>
