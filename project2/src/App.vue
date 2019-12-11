<template>
  <div>
    <h1 v-once>{{ title }}</h1>
    <p>{{ getTitle() }}</p>
    <a v-bind:href="url">Google</a>
    <p v-html="link"></p>
    <counter />
  </div>
</template>

<script>
import Counter from "@/components/Counter";
import { link } from "fs";
export default {
  name: "app",
  components: {
    counter: Counter
  },
  data() {
    return {
      title: "Some title",
      url: "https://google.com",
      link: '<a href="https://google.com">Google</a>'
    };
  },
  methods: {
    getTitle() {
      this.title = "Some other title";
      return this.title;
    }
  }
};
</script>

