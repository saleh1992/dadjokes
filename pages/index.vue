<template>
  <div>
    {{ Jokes.joke }}<br>
    <button @click="getData()">again</button>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  head() {
    return {
      title: "welcome in dadjokes",
      meta: [
        {
          hid: 'this is hid dadjokes',
          name: "this is name of dadjokes",
          description: " this is description",
          dammy: "dammy"
        }
      ],
    }
  },
  data: () => ({
    Jokes: [],

  }),
  methods: {
    async getData() {
      const config = {
        headers: {
          Accept: 'application/json'
        }
      }
      try {
        const res = await this.$axios.$get('https://icanhazdadjoke.com/', config);
        this.Jokes = res
        console.log(res);
      }
      catch (error) {
        console.log(error);
      }
    }
  },
  mounted() {
    this.getData()

  }

}
</script>

<!-- <style lang="scss">
@import "../scss/core.scss";
@import "../scss/variables.scss";
</style> -->
