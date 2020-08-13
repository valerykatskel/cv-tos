<template>
  <div class="cv-section cv-header">
    <div class="header-left">
      <h2>{{ data.name }}</h2>
      <h3>{{ data.position }}</h3>
      <p>{{ age }}, {{ data.location }}</p>

      <ul class="cv-contact-info">
        <li>E-mail: ne.vse.srazu@gmail.com</li>
        <li>Skype: bestnickname</li>
        <li>Phone/WhatsApp/Telegram/Viber: +375 29 768 86 32</li>
      </ul>
    </div>
    <div class="header-right">
      <img src="@/assets/photo.jpg" alt />
    </div>
  </div>
</template>

<script>
import { Header } from "../data/data";
export default {
  name: "CvHeader",

  data() {
    return {
      data: {}
    };
  },
  computed: {
    age() {
      return `${new Date().getFullYear() - this.data.yob} years old`;
    }
  },
  mounted() {
    this.$nextTick(() => {
      this.data = { ...Header };
    });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h2,
h3 {
  font-weight: 400;
  color: rgba(0, 0, 0, 0.9);
}
h2 {
  font-size: 3.2rem;
  line-height: 1.25;
}
.cv-header {
  display: flex;
  justify-content: space-between;

  .header-right {
    margin-top: 15px;
    margin-bottom: 15px;

    img {
      height: 165px;
      vertical-align: bottom;
    }
  }

  .header-left {
    h2 {
      margin-top: 5px;
    }
  }
}
.cv-contact-info {
  margin: 16px 0 16px 16px;
  padding: 0;
  li {
    font-size: 14px;
  }
}
</style>
