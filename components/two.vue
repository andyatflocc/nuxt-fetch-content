<template>
  <div style="border: 1px dotted; width: 100%; padding: 50px; margin: 20px">
    <p>{{ example2 }}</p>
    <p>list of things:</p>
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
    this.example2 = "updated by fetch 2";
    this.items = await this.$content('things').fetch()

  },
};
</script>