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
      class="card"
      v-for="card in arrWhatWeDo"
      :key="card"
      :data="card"
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
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}

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
