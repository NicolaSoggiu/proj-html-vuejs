<script>
import AppCard from "./AppCard.vue";

export default {
  data() {
    return {
      arrWhatWeDo: [
        {
          img: "../../public/img/image14.svg",
          title: "ARRAY OF EQUIPMENT",
          text: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
        },
        {
          img: "../../public/img/image15.svg",
          title: "NEW TECHNOLOGIES",
          text: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
        },
        {
          img: "../../public/img/image16.svg",
          title: "VERSITILE ACTORS",
          text: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
        },
        {
          img: "../../public/img/image17.svg",
          title: "TOP DIRECTORS",
          text: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
        },
        {
          img: "../../public/img/image18.svg",
          title: "MINUTE EDITING",
          text: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
        },
        {
          img: "../../public/img/image19.svg",
          title: "VERSITILE ACTORS",
          text: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
        },
      ],
    };
  },
  components: {
    AppCard,
  },
};
</script>

<template>
  <div class="What-we-do">
    <AppCard v-for="card in arrWhatWeDo" :key="card" :card="card" />
  </div>
</template>

<style lang="scss" scoped>
.what-we-do {
  display: flex;
}
</style>
