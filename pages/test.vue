<template>
  <div>
    <One />
    <Two />
    <nuxt-link to="/">Home</nuxt-link>
  </div>
</template>

<script>
import One from "~/components/one.vue";
import Two from "~/components/two.vue";

export default {
  components: {
    One,
    Two,
  },
};
</script>