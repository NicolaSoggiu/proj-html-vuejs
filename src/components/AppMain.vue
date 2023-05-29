<script>
import AppWhatWeDo from "./AppWhatWeDo.vue";

export default {
  components: {
    AppWhatWeDo,
  },
};
</script>

<template>
  <main>
    <div class="jumbotron">
      <div class="left-arrow">
        <font-awesome-icon :icon="['fass', 'arrow-left']" />
      </div>
      <div class="jumbo-title">
        <span>CINEMATO STUDIO</span>
        <h1>
          ACTION AND <br />
          ISPIRE PEOPLE
        </h1>
        <span class="jumbo-read-more">READ MORE</span>
      </div>
      <div class="right-arrow">
        <font-awesome-icon :icon="['fas', 'arrow-right']" />
      </div>
    </div>
    <AppWhatWeDo />
  </main>
</template>

<style lang="scss" scoped>
.jumbotron {
  height: 75vh;
  margin: 0.5rem;
  background-image: url(../../public/img/blog05.jpg);
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: white;
  h1 {
    font-size: 4rem;
    padding-bottom: 1.5rem;
  }

  .jumbo-title {
    margin-right: 25rem;
    .jumbo-read-more {
      padding: 0.5rem 1rem;
      color: black;
      background-color: white;
      font-size: 0.7rem;
      cursor: pointer;
    }
  }

  .left-arrow,
  .right-arrow {
    font-size: 1.5rem;
    padding: 0.5rem 0.7rem;
    background-color: black;
    opacity: 0.6;
    cursor: pointer;
  }

  .left-arrow {
    margin-left: 1rem;
  }

  .right-arrow {
    margin-right: 1rem;
  }
}
</style>
