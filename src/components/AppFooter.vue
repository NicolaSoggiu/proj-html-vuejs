<script>
export default {
  data() {
    return {
      arrContact: [
        {
          title: "CONTACT INFO",
          location: "2/45 Tower Street, New York USA",
          number: "Call Us On 0800 840 1010",
          mail: "Demo@Example.Com",
        },
      ],
      arrInfo: [
        {
          title: "INFORMATION",
          voice1: "Product Support",
          voice2: "Checkout",
          voice3: "Report Abuse",
          voice4: "Redeem Voucher",
          voice5: "Order Status",
        },
      ],
      arrLinks: [
        {
          title: "USEFUL LINKS",
          voice1: "Policies & Rules",
          voice2: "Privacy Policy",
          voice3: "License Policy",
          voice4: "My Account",
          voice5: "Locality,",
        },
      ],
    };
  },
};
</script>

<template>
  <footer>
    <div class="footer-container">
      <div class="footer-column">
        <h3>{{ arrContact[0].title }}</h3>
        <ul>
          <li>
            <font-awesome-icon
              class="footer-icon"
              :icon="['fas', 'location-dot']"
            />
            {{ arrContact[0].location }}
          </li>
          <li>
            <font-awesome-icon class="footer-icon" :icon="['fas', 'phone']" />
            {{ arrContact[0].number }}
          </li>
          <li>
            <font-awesome-icon
              class="footer-icon"
              :icon="['fas', 'envelope']"
            />
            {{ arrContact[0].mail }}
          </li>
        </ul>
      </div>
      <div class="footer-column">
        <h3>{{ arrInfo[0].title }}</h3>
        <ul>
          <li>{{ arrInfo[0].voice1 }}</li>
          <li>{{ arrInfo[0].voice2 }}</li>
          <li>{{ arrInfo[0].voice3 }}</li>
          <li>{{ arrInfo[0].voice4 }}</li>
          <li>{{ arrInfo[0].voice5 }}</li>
        </ul>
      </div>
      <div class="footer-column">
        <h3>{{ arrLinks[0].title }}</h3>
        <ul>
          <li>{{ arrLinks[0].voice1 }}</li>
          <li>{{ arrLinks[0].voice2 }}</li>
          <li>{{ arrLinks[0].voice3 }}</li>
          <li>{{ arrLinks[0].voice4 }}</li>
          <li>{{ arrLinks[0].voice5 }}</li>
        </ul>
      </div>
      <div class="footer-column">
        <h3>NEWSLETTER</h3>
        <ul>
          <li class="newsletter-text">
            Subscribe To Receive Inspiration, Ideas & News In Your Inbox.
          </li>
        </ul>
        <div class="form">
          <input type="text" placeholder="Enter Your Email" />
          <button class="btn">SUBSCRIBE</button>
        </div>
      </div>
    </div>
    <div class="license">
      <div class="line"></div>
      <span> &copy; 2023 All Rights Reserved. Developed By TemplateMela</span>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
footer {
  height: 60vh;
  background-color: #111111;
}

.footer-container {
  width: 1000px;
  margin: auto;
  display: flex;
  justify-content: space-around;
  align-items: start;
  height: 100%;
  color: white;
  padding: 0 0.5rem;
  gap: 2rem;
  .footer-column {
    text-align: left;
    padding-top: 6rem;
    flex: 0 0 25%;
    .form {
      display: flex;
      flex-direction: column;
    }
  }
}

.footer-column h3 {
  font-size: 1rem;
  margin-bottom: 1rem;
}

.footer-column p,
.footer-column ul {
  font-size: 0.8rem;
  margin-bottom: 1rem;
}

.footer-column li {
  list-style: none;
  padding: 0.4rem 0;
  color: lightgrey;
  &:hover {
    color: white;
    cursor: pointer;
  }
}
.footer-icon {
  padding-right: 1rem;
}
.newsletter-text {
  line-height: 1.5rem;
}

.form input {
  background-color: #1c1c1c;
  color: lightgrey;
  padding: 0.5rem 1rem;
  margin-bottom: 0.5rem;
  border: 0;
}

.btn {
  width: 150px;
  padding: 0.5rem;
}

.license {
  background-color: #111111;
  color: white;
  text-align: center;
  padding: 2rem 0;
  .line {
    height: 1px;
    background-color: grey;
    width: 70%;
    margin: 0 auto;
    margin-bottom: 2rem;
  }
}
</style>
