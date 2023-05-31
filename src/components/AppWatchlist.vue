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
  methods: {
    getCardClass(index) {
      const image = "imgclass1";
      return image;
    },
  },
  components: {
    AppCard,
  },
};
</script>

<template>
  <div>
    <div class="text">
      <span>YOUR WATCHLIST</span>
      <h1>BEST HITS MOVIES</h1>
    </div>
    <div class="watchlist">
      <AppCard
        v-for="(watch, index) in arrWatchList"
        :key="watch.title"
        :data="watch"
        :img-class="getCardClass(index)"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.text {
  text-align: center;
  span {
    font-size: 0.7rem;
  }
  h1 {
    margin-top: 1rem;
    margin-bottom: 2rem;
  }
}

.watchlist {
  width: 1000px;
  margin: auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 3rem;
  justify-items: center;
  text-align: center;
  margin-top: 4rem;
  margin-bottom: 4rem;
}

h2 {
  padding-bottom: 1rem;
  font-size: 1rem;
}
span {
  font-size: 0.6rem;
}
</style>
