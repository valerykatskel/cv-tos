<template>
  <div id="app">
    <my-cv />
  </div>
</template>

<script>
import MyCv from "./components/MyCv.vue";

export default {
  name: "App",
  components: {
    MyCv
  }
};
</script>

<style lang="scss">
:root,
body,
html {
  margin: 0;
  padding: 0;
  background-color: #f5f5f5;
  box-sizing: border-box;
}
body {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, Segoe UI, Roboto,
    Helvetica Neue, Fira Sans, Ubuntu, Oxygen, Oxygen Sans, Cantarell,
    Droid Sans, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol,
    Lucida Grande, Helvetica, Arial, sans-serif;
}
body,
h1,
p {
  font-weight: 400;
  color: rgba(0, 0, 0, 0.9);
}
body,
p {
  font-size: 1.6rem;
  line-height: 1.5;
}
.cv-section {
  position: relative;
  padding: 0 48px;
  margin-bottom: 24px;
  border-bottom: 1px solid rgba(0, 0, 0, 0.15);
}
</style>
