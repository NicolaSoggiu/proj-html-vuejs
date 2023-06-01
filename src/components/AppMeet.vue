<script>
import AppCard from "./AppCard.vue";

export default {
  data() {
    return {
      arrMeet: [
        {
          img: "/img/Team-01.jpg",
          title: "FABRICIO GUERRA",
          text: "Main Director",
        },
        {
          img: "/img/Team-02.jpg",
          title: "UMBERTO PAGODA",
          text: "Main Writer",
        },
        {
          img: "/img/Team-03.jpg",
          title: "GLORIA RICASSO",
          text: "Main Producer",
        },
        {
          img: "/img/Team-04.jpg",
          title: "LIO NAPOIN",
          text: "Cameraman",
        },
      ],
    };
  },
  methods: {
    getCardClass(index) {
      const image = "imgclass2";
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
    <span>THE PERICUROS</span>
    <h1>MEET THE TEAM</h1>
  </div>
  <div class="meet-team">
    <AppCard
      v-for="(team, index) in arrMeet"
      :key="team"
      :data="team"
      :img-class="getCardClass(index)"
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

.meet-team {
  display: flex;
  justify-content: center;
  gap: 1rem;
  padding-inline: 15rem;
  margin-top: 4rem;
  margin-bottom: 4rem;
}
</style>
