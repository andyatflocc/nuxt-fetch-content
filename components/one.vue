<template>
  <div style="border: 1px dotted; width: 100%; padding: 50px; margin: 20px">
    <p>{{ example }}</p>
    <p>list of stuff:</p>
    <ul>
    <li v-for="item in items" :key="item.title">{{ item.title}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      example: "initial value",
      items: []
    };
  },
  async fetch() {
    this.example = "updated by fetch";
    this.items = await this.$content('stuff').fetch()

  },
};
</script>