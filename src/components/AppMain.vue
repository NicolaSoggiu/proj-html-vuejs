<script>
export default {};
</script>

<template>
  <main>
    <div class="jumbotron">
      <div class="left-arrow">
        <img src="../../public/img/left-arrow.svg" alt="" />
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
        <img src="../../public/img/right-arrow.svg" alt="" />
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
    margin-right: 28rem;
  }
  .jumbo-read-more {
    padding: 0.5rem 1rem;
    color: black;
    background-color: white;
    font-size: 0.7rem;
    cursor: pointer;
  }
}
</style>
