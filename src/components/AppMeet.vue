<script>
import AppCard from "./AppCard.vue";

export default {
  data() {
    return {
      arrMeet: [
        {
          img: "../../public/img/Gallery-01.jpg",
          title: "FABRICIO GUERRA",
          text: "Main Director",
        },
        {
          img: "../../public/img/Gallery-02.jpg",
          title: "UMBERTO PAGODA",
          text: "Main Writer",
        },
        {
          img: "../../public/img/Gallery-03.jpg",
          title: "GLORIA RICASSO",
          text: "Main Producer",
        },
        {
          img: "../../public/img/Gallery-04.jpg",
          title: "LIO NAPOIN",
          text: "Cameraman",
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
    <span>THE PERICUROS</span>
    <h1>MEET THE TEAM</h1>
  </div>
  <div class="meet-team">
    <AppCard v-for="team in arrMeet" :key="team" :data="team" />
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
  padding-inline: 15rem;
  margin-top: 4rem;
  margin-bottom: 4rem;
}
</style>
