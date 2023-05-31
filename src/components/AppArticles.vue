<script>
import AppCard from "./AppCard.vue";

export default {
  data() {
    return {
      arrArticles: [
        {
          img: "../../public/img/blog07.jpg",
          date: "November 06, 2021 by Admin",
          title: "RECAP YOUR LATEST COMPANY EVENT",
          text: "Suspendisse dictum tempor. Ut non faucibus arcu, id elementum est. Suspendisse sed",
        },
        {
          img: "../../public/img/blog01.jpg",
          date: "May 27, 2022 by Admin",
          title: "HOW TO EDIT A FILM SCORE TO SERVE",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incidudnt ut",
        },
        {
          img: "../../public/img/blog02.jpg",
          date: "May 07, 2022 by Admin",
          title: "ARE YOU READY TO MAKE IT AWESOME",
          text: "Design is our playground. While we create an awesome experience, we like having fun. No animals",
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
    <span>LATEST NEWS</span>
    <h1>ARTICLES UPDATE DAILY</h1>
  </div>
  <div class="articles">
    <AppCard
      class="card"
      v-for="article in arrArticles"
      :key="article"
      :data="article"
    />
  </div>
</template>

<style lang="scss" scoped>
.text {
  text-align: center;
  margin-top: 4rem;
  span {
    font-size: 0.7rem;
  }
  h1 {
    margin-top: 1rem;
    margin-bottom: 2rem;
  }
}

.articles {
  display: flex;
  justify-content: center;
  gap: 1rem;
  padding-inline: 12rem;
  margin-top: 4rem;
  margin-bottom: 4rem;
  .card {
    width: calc((100% / 3) - 2rem);
    display: flex;
    flex-direction: column;
    text-align: left;
  }
}
</style>
