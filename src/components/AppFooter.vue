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
          title: "Information",
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
        <p>{{ arrContact[0].location }}</p>
        <p>{{ arrContact[0].number }}</p>
        <p>{{ arrContact[0].mail }}</p>
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
          <li>Subscribe To Receive Inspiration,</li>
          <li>Ideas & News In Your Inbox.</li>
        </ul>
        <div class="form">
          <input type="text" placeholder="Enter Your Email" />
          <button>SUBSCRIBE</button>
        </div>
      </div>
    </div>
    <div class="license">
      <span>2023 All Rights Reserved. Developed By TemplateMela</span>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
footer {
  height: 60vh;
  background-color: #111111;
}

.footer-container {
  display: flex;
  justify-content: space-around;
  align-items: center;
  height: 100%;
  color: white;
}

.footer-column {
  text-align: left;
  .form {
    display: flex;
    flex-direction: column;
  }
}

.footer-column h3 {
  font-size: 1.2rem;
  margin-bottom: 1rem;
}

.footer-column p,
.footer-column ul {
  font-size: 0.8rem;
  margin-bottom: 0.5rem;
}

.footer-column li {
  list-style: none;
}

.license {
  background-color: #111111;
  color: white;
  text-align: center;
  padding: 2rem 0;
}
</style>
