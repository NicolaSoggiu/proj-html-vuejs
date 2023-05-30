<script>
import AppCard from "./AppCard.vue";

export default {
  data() {
    return {
      arrWatchList: [
        {
          img: "../../public/img/Gallery-01.jpg",
          title: "SEVENTEENTH SUMMER",
          text: "Commercial, Music Video.",
        },
        {
          img: "../../public/img/Gallery-02.jpg",
          title: "A MESSAGE TO SPACE",
          text: "Short Film",
        },
        {
          img: "../../public/img/Gallery-03.jpg",
          title: "THE MOST BEAUTIFUL THING",
          text: "Music Video",
        },
        {
          img: "../../public/img/Gallery-04.jpg",
          title: "PERMISSION TO SPEAK",
          text: "Documentary",
        },
        {
          img: "../../public/img/Gallery-05.jpg",
          title: "EXPLORE OUR SPACE",
          text: "Film noir",
        },
        {
          img: "../../public/img/Gallery-06.jpg",
          title: "FILM PRODUCTION",
          text: "Blaxploitation",
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
  <div class="watchlist">
    <AppCard v-for="card in arrWatchList" :key="card" :card="watch" />
  </div>
</template>

<style lang="scss" scoped></style>
