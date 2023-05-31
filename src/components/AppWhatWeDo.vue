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
          img: "../../public/img/image16.svg",
          title: "NEW TECHNOLOGIES",
          text: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
        },
        {
          img: "../../public/img/image18.svg",
          title: "VERSITILE ACTORS",
          text: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
        },
        {
          img: "../../public/img/image15.svg",
          title: "TOP DIRECTORS",
          text: "Lorem ipsum dolor amet, consectetur adipiscing. Pellentesque ultricies justo tellus.",
        },
        {
          img: "../../public/img/image17.svg",
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
  methods: {
    getCardClass(index) {
      const image = "imgclass3";
      return image;
    },
  },
  components: {
    AppCard,
  },
};
</script>

<template>
  <div class="text">
    <span>PELICULA STUDIO</span>
    <h2>THIS IS WHAT WE DO</h2>
  </div>
  <div class="What-we-do">
    <AppCard
      v-for="(card, index) in arrWhatWeDo"
      :key="card"
      :data="card"
      :img-class="getCardClass(index)"
    />
  </div>
</template>

<style lang="scss" scoped>
.text {
  text-align: center;
  padding-top: 3rem;
  span {
    font-size: 0.7rem;
    margin-bottom: 1rem;
  }
  h2 {
    padding-top: 1rem;
    padding-bottom: 2rem;
  }
}

.What-we-do {
  width: 1000px;
  margin: auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 3rem;
  align-items: center;
  text-align: center;
  margin-top: 1rem;
  margin-bottom: 4rem;
}
</style>
