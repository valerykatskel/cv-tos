<template>
  <div v-if="data.length > 0" class="cv-section">
    <h3 class="t-18 t-black t-bold">Education</h3>

    <ul class="pv-accomplishments-block__list pv-accomplishments-block__list--has-more">
      <li
        class="resume-builder__subsection-container"
        v-for="item in data"
        :key="item.id"
        :item="item"
      >
        <img
          width="24"
          :src="item.logo"
          loading="lazy"
          height="24"
          :alt="getLogoAlt(item.name)"
          class="flex-shrink-zero mr2 lazy-image ember-view"
        />
        <div class="full-width">
          <h4 class="t-16 t-black t-bold">{{ item.position }}</h4>
          <p class="t-16 t-black">{{ item.name }}</p>
          <p class="t-14 t-black">{{ duration }}</p>
          <p class="white-space-pre-wrap break-words t-14 t-black">
            <span dir="ltr" v-html="item.description" />
          </p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import { Experience } from "../data/data";
export default {
  name: "CvEducation",
  data() {
    return {
      data: {}
    };
  },
  methods: {
    getLogoAlt(name) {
      return `Logo for ${name}`;
    }
  },
  computed: {
    duration() {
      return this.data.end === ""
        ? `${this.data.start} – Present`
        : `${this.data.start} – ${this.data.end}`;
    }
  },
  mounted() {
    this.$nextTick(() => {
      this.data = Experience;
    });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
