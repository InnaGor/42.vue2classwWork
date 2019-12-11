<template>
  <div>
    <h1>{{ counter }}</h1>
    <br />
    <!-- <button v-on:click="IncreaseCounter">Increase counter</button> -->
    <form action="https://google.com">
      <input type="submit" v-on:click.prevent="IncreaseCounter" value="Increase counter" />
    </form>
  </div>
</template>

<script>
// v-[directive]:[attribute].[modifier]
export default {
  name: "Counter",
  data() {
    return {
      counter: 0
    };
  },
  methods: {
    IncreaseCounter() {
      this.counter++;
    }
  }
};
</script>