<template>
  <div class="cv-section cv-header">
    <div class="header-left">
      <h2>{{ data.name }}</h2>
      <p>{{ age }}, {{ data.location }}</p>
      <p>{{ data.position }}</p>

      <div class="display-flex flex-wrap mt4 mb2">
        <div class="resume-builder-contact-info__field-container">
          <li-icon
            type="envelope-open-icon"
            class="resume-builder-contact-info__email-icon"
            size="small"
            role="img"
            aria-label="Email"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 16 16"
              data-supported-dps="16x16"
              fill="currentColor"
              width="16"
              height="16"
              focusable="false"
            >
              <path
                d="M14.5 3.56L8.5.13A1 1 0 008 0a1 1 0 00-.5.13l-6 3.43a1 1 0 00-.5.87V12a1 1 0 001 1h12a1 1 0 001-1V4.43a1 1 0 00-.5-.87zM8 2.15L13 5v.1L8.31 8a.57.57 0 01-.64 0L3 5.11V5zM3 11V6.14l4.2 2.6A1.44 1.44 0 008 9a1.41 1.41 0 00.78-.24L13 6.14V11H3z"
              />
            </svg>
          </li-icon>
          <p class="t-14 t-black">ne.vse.srazu@gmail.com</p>
        </div>
        <div class="resume-builder-contact-info__field-container">
          <li-icon
            type="phone-handset-icon"
            class="mr1 ghosted"
            size="small"
            role="img"
            aria-label="Phone number"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 16 16"
              data-supported-dps="16x16"
              fill="currentColor"
              width="16"
              height="16"
              focusable="false"
            >
              <path
                d="M4.18 11.82C6.62 14.26 8.64 15 10.79 15a3.76 3.76 0 002.66-1.1l1.32-1.32a.8.8 0 000-1.13L11.6 8.29a1 1 0 00-.69-.29 1 1 0 00-.42.09l-1.67.73-1.64-1.64.73-1.67A1 1 0 008 5.09a1 1 0 00-.29-.69L4.55 1.23a.8.8 0 00-1.13 0L2.1 2.55A3.76 3.76 0 001 5.21c0 2.15.74 4.17 3.18 6.61zm1.24-1.24c-2.34-2.34-2.67-4-2.67-5.37a2 2 0 01.59-1.42L4 3.14l2 2-1 2.32L8.54 11l2.29-1 2 2-.65.65a2 2 0 01-1.42.59c-1.38.01-3-.31-5.34-2.66z"
              />
            </svg>
          </li-icon>
          <p class="t-14 t-black">+375297688632</p>
        </div>
        <div class="resume-builder-contact-info__field-container">
          <li-icon
            type="linkedin-inbug-color-icon"
            class="mr1"
            size="small"
            role="img"
            aria-label="LinkedIn profile"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 16 16"
              data-supported-dps="16x16"
              width="16"
              height="16"
              focusable="false"
            >
              <path
                d="M13.75 1H2.25A1.25 1.25 0 001 2.25v11.5A1.25 1.25 0 002.25 15h11.5A1.25 1.25 0 0015 13.75V2.25A1.25 1.25 0 0013.75 1z"
                fill="#0073b1"
              />
              <path
                d="M4 2.68A1.36 1.36 0 002.69 4 1.36 1.36 0 004 5.31 1.36 1.36 0 005.31 4 1.36 1.36 0 004 2.68zM3 6h2v7H3zM10.25 5.88a3 3 0 00-2.31 1h-.06V6H6v7h2v-3c0-1.17.48-2 1.62-2 .91 0 1.38.66 1.38 2v3h2V8.88c0-1.88-.79-3-2.75-3z"
                fill="#fff"
              />
            </svg>
          </li-icon>
          <a
            href="https://www.linkedin.com/in/valerykatskel/"
            id="ember2519"
            class="link-without-hover-visited t-14 ember-view"
          >linkedin.com/in/valerykatskel</a>
        </div>

        <div class="resume-builder-contact-info__field-container">
          <li-icon
            type="linkedin-inbug-color-icon"
            class="mr1"
            size="small"
            role="img"
            aria-label="LinkedIn profile"
          >
            <svg
              class="octicon octicon-mark-github v-align-middle"
              height="18"
              viewBox="0 0 16 16"
              version="1.1"
              width="18"
              aria-hidden="true"
            >
              <path
                fill-rule="evenodd"
                d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"
              />
            </svg>
          </li-icon>
          <a
            href="https://github.com/valerykatskel"
            id="ember2519"
            class="link-without-hover-visited t-14 ember-view"
          >github.com/valerykatskel</a>
        </div>
      </div>
    </div>
    <div class="header-right">
      <img src="@/assets/photo.png" alt />
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
    padding-top: 10px;
  }
}
</style>
