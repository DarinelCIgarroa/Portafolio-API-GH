<template>
  <a :href="url_redirect" target="_blank" :class="setColor">{{ title }}</a>
</template>
<script>
export default {
  name: "ButtonComponent",
  props: {
    color: String,
    url_redirect: String,
    title: {
      type: String,
      default: "Repository",
    },
  },
  computed: {
    setColor() {
      return this.color === "dark" ? "btn btn-dark m-2" : "btn btn-danger m-2";
    },
  },
};
</script>