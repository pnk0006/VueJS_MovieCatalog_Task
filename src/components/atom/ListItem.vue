<template>
  <a href="#" :class="{ active: selected }">
    {{ title }}
  </a>
</template>

<script>
export default {
  name: "ListItem",
  props: {
    title: String,
    selected: Boolean,
  },
};
</script>

<style scoped>
a {
  background-color: #ececec;
  font-weight: normal;
  cursor: pointer;
  padding-left: 0.75em;
  padding-right: 0.75em;
  padding-top: 0.2em;
  padding-bottom: 0.2em;
  color: #1a1a1a;
  text-decoration: none;
  width: 100%;
  display: block;
}
a.active {
  background-color: #a9b3c4;
  font-weight: bold;
}
</style>