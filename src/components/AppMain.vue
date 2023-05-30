<script>
import AppWatchlist from "./AppWatchlist.vue";
import AppWhatWeDo from "./AppWhatWeDo.vue";
import AppMeet from "./AppMeet.vue";
import AppArticles from "./AppArticles.vue";

export default {
  data() {
    return {
      arrStats: [
        {
          number: "158",
          text: "SATISFIED CLIENTS",
        },
        {
          number: "3+",
          text: "OUR PROJECTS",
        },
        {
          number: "1,906",
          text: "CUP OF COFFEE",
        },
        {
          number: "2",
          text: "OUR AWARDS",
        },
      ],
      arrLogos: [
        {
          img: "../../public/img/03.png",
        },
        {
          img: "../../public/img/04.png",
        },
        {
          img: "../../public/img/05.png",
        },
        {
          img: "../../public/img/01.png",
        },
        {
          img: "../../public/img/02.png",
        },
      ],
    };
  },
  components: {
    AppWhatWeDo,
    AppWatchlist,
    AppMeet,
    AppArticles,
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
    <AppWatchlist />
    <div class="stats">
      <div class="info" v-for="info in arrStats" :key="info">
        <h1>{{ info.number }}</h1>
        <span>{{ info.text }}</span>
      </div>
    </div>
    <AppMeet />
    <div class="testimonials">
      <div class="testimonials-text">
        <font-awesome-icon
          class="quote-icon"
          :icon="['fas', 'quote-left']"
          style="color: #fcfcfd"
        />
        <span
          >Curabitur bibendum ex ut sapien blandit viverra. Nunc lobartis mi
          dui, id Etiam tempor sit amet metus in bibendum. Nunc eros risus,
          pellentesque a augue Pellentesque fringilla eget mi eu mollis. Mauris
          commodo.</span
        >
      </div>
      <div class="employees">
        <img src="../../public/img/01.jpg" alt="" />
        <div class="employees-info">
          <span>JOHN DOE</span>
          <span>Designer</span>
        </div>
      </div>
    </div>
    <AppArticles />
    <div class="logos">
      <img v-for="logo in arrLogos" :key="logo" :src="logo.img" alt="" />
    </div>
    <div class="collaborate">
      <div class="left">
        <span>COLLABORATE</span>
        <h1>WANT TO WORK WITH US? LEAVE US A MESSAGE!</h1>
        <span
          >Duis sit amet congue ipsum. Nulla maximus My venenatinos posuere. To
          The Mauris ut tempus Suspendisse porta tincidunt lecturs non of me
          pellentesque. At A Sed blandit at diam sit amet Orci varius natoque
          penatibus et dis dis to parturient montes, My Car nascentur ridiculus
          Sed feugiat locus in erat egestas, quis eleifend lacus imperdiet</span
        >
      </div>
      <div class="right">
        <div class="name">
          <input type="text" name="" id="" placeholder="Your Name" />
          <input type="text" name="" id="" placeholder="Your Email" />
        </div>
        <div class="number">
          <input type="text" name="" id="" placeholder="Mobile Number" />
          <input type="text" name="" id="" placeholder="Your Pincode" />
        </div>
        <input type="text" class="message" placeholder="Enter your Message" />
        <button class="sub-button">Submit Now</button>
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

.stats {
  height: 35vh;
  margin: 0.5rem;
  background-image: url(../../public/img/Parallax-01.jpg);
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  gap: 5rem;
  justify-content: center;
  align-items: center;
  color: white;
  .info {
    display: flex;
    flex-direction: column;
    align-items: center;
    h1 {
      padding-bottom: 0.5rem;
    }
  }
}

.testimonials {
  height: 70vh;
  margin: 0.5rem;
  margin-top: 4rem;
  background-image: url(../../public/img/Parallax-02.jpg);
  background-size: cover;
  .testimonials-text {
    padding-top: 6rem;
    padding-bottom: 1rem;
    padding-inline: 25rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    color: white;
    text-align: center;
    line-height: 2rem;
    .quote-icon {
      font-size: 70px;
    }
  }
  .employees {
    display: flex;
    justify-content: center;
    img {
      border-radius: 40px;
      margin-right: 0.5rem;
    }
    .employees-info {
      display: flex;
      flex-direction: column;
      justify-content: center;
      color: white;
    }
  }
}

.logos {
  height: 35vh;
  margin: 0.5rem;
  background-image: url(../../public/img/Parallax-03.jpg);
  background-size: cover;
  background-position: center;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 6rem;
  img {
    width: 100px;
  }
}

.collaborate {
  display: flex;
  justify-content: space-around;
  padding: 5rem 15rem;
  gap: 3rem;
  margin: auto;
  .left {
    display: flex;
    flex-direction: column;
    flex: 0 0 55%;
    h1 {
      margin: 1rem 0;
    }
    span {
      font-size: 0.7rem;
      line-height: 1.5rem;
    }
  }
  .right {
    display: flex;
    flex-direction: column;
    .name,
    .number {
      display: flex;
      gap: 1rem;
      flex-grow: 1;
    }
    input {
      background-color: #f2f2f2;
      border: #f2f2f2;
      padding: 0.5rem;
      padding-right: 5rem;
    }
    .name {
      margin-top: 3rem;
      margin-bottom: 1.5rem;
    }
    .number {
      margin-bottom: 1.5rem;
    }
    .message {
      padding-bottom: 9rem;
      margin-bottom: 1rem;
    }
    .sub-button {
      background-color: black;
      color: white;
      padding: 0.5rem 0;
      cursor: pointer;
    }
  }
}
</style>
