<template>
  <header class="header">
    <h1 class="title">Dad Jokes</h1>
    <ul>
      <li>
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/jokes">Jokes</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about">About</nuxt-link>
      </li>
    </ul>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  head() {
    return {
      title: "welcome in AppHeader",
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
}
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #ffffff;
  padding: 5px 25px;
  border-radius: 7px;
}

ul {
  display: flex;
  justify-content: space-between;
  padding: 0;
  width: 215px;
}

li {
  list-style: none;
}

a {
  text-decoration: none;
  padding: 5px 11px;
  background: gray;
  color: white;
}
</style>
