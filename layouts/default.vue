<template>
  <div>
    <navbar/>
    <nuxt/>
    <foot/>
  </div>
</template>

<script>
import navbar from "~/components/Navbar.vue";
import foot from "~/components/Footer.vue";

export default {
  components: {
    navbar,
    foot
  },
  // vue js provides us `mounted()`. this means `onload` in javascript.
  // mounted: {
  // }
};
</script>

<style>
</style>
