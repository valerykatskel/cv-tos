<template>
  <div v-if="data.length > 0" class="cv-section">
    <h3 class="t-18 t-black t-bold">Achievements</h3>
    <div class="header-achievements">
      <ul class="cv-section-items is-bulleted">
        <li v-for="item in data" :key="item">
          <span v-html="item"></span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import { Achievements } from "../data/data";
export default {
  name: "CvAchievements",

  data() {
    return {
      data: {}
    };
  },
  mounted() {
    this.$nextTick(() => {
      this.data = Achievements;
    });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss"></style>
