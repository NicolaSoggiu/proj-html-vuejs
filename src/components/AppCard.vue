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
    <span class="date">{{ data.date }}</span>
    <h2>{{ data.title }}</h2>
    <span>{{ data.text }}</span>
  </div>
</template>

<style lang="scss" scoped>
.imgclass1 {
  width: 320px;
}

.imgclass2 {
  width: 250px;
}

.imgclass3 {
  width: 60px;
}

h2 {
  margin-top: 1rem;
  margin-bottom: 0.5rem;
}

span {
  color: grey;
  margin-top: 1rem;
}

.date {
  font-size: 0.7rem;
}
</style>
