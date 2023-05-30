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
    <div class="About-us">
      <div class="about-text">
        <span>ABOUT US</span>
        <h1>HIGH QUALITY CINEMATICS</h1>
        <span class="about-description"
          >Orci varius penatibus et magnis dis parturient in the montes,
          nascetur ridiculis mus. Nulla A nisi ut mi efficitur hendrerit. nunc
          urna. quisque a partr hendrerit purus erat, nec dapibus sem sed.
          phasellus sed eli molestie, partitor ligula of the egesas, mattis
          augue. quisque et rhoncus justo. suspendisse luctus pharetra
          elemetcondimentum.</span
        >
        <span class="about-read-more">READ MORE</span>
      </div>
    </div>
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

.About-us {
  height: 70vh;
  margin: 0.5rem;
  margin-top: 4rem;
  background-image: url(../../public/img/About-Us.jpg);
  background-size: contain;
  background-repeat: no-repeat;
  color: white;
  .about-text {
    margin-left: 40rem;
    margin-right: 10rem;
    padding-top: 5rem;
    span {
      font-size: 0.7rem;
      padding-bottom: 2rem;
    }
    h1 {
      padding: 1rem 0;
    }
    .about-description {
      display: block;
    }
    .about-read-more {
      padding: 0.5rem 1rem;
      color: black;
      background-color: white;
      font-size: 0.7rem;
      cursor: pointer;
    }
  }
}
</style>
