<template>
  <div v-if="data.length > 0" class="cv-section">
    <h3 class="t-18 t-black t-bold">Experience</h3>

    <ul
      class="pv-accomplishments-block__list pv-accomplishments-block__list--has-more"
    >
      <li
        class="cv-section-item"
        v-for="item in data"
        :key="item.id"
        :item="item"
      >
        <div class="full-width">
          <h4 class="t-16 t-black t-bold">{{ item.position }}</h4>
          <p class="t-16 t-black">
            {{ item.name }}
            <span
              v-show="item.type !== undefined && item.type.trim().length > 0"
              class="pv-entity__secondary-title separator"
              >{{ item.type }}</span
            >
          </p>
          <p class="t-14 t-black">
            {{ getDuration(item.start, item.end) }}
            <span
              v-show="
                item.location !== undefined && item.location.trim().length > 0
              "
              class="pv-entity__secondary-title separator"
              >{{ item.location }}</span
            >
          </p>

          <p
            class="white-space-pre-wrap break-words t-14 t-black item-description"
          >
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
  name: "CvExperience",
  data() {
    return {
      data: {}
    };
  },
  methods: {
    getLogoAlt(name) {
      return `Logo for ${name}`;
    },
    getDuration(start, end) {
      return end === "" ? `${start} – Present` : `${start} – ${end}`;
    }
  },
  computed: {},
  mounted() {
    this.$nextTick(() => {
      this.data = Experience;
    });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.pv-entity__secondary-title.separator::before {
  content: "\00B7";
  padding: 0 4px 0 0;
}
.item-description {
  margin-top: 15px;
}
</style>
