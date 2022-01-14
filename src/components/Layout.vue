<template>
  <div id="app">
    <div id="main-nav">
      <div id="logo"><img src="" alt="Logo">
      </div>
      <router-link to="/">HOME</router-link> |
      <router-link to="/menu">GAMES</router-link> |
      <router-link to="/1">CHAT</router-link> |
      <router-link to="/store">STORE</router-link> |
      <router-link to="/profile">PROFILE</router-link> |
      <router-link to="/4">SETTINGS</router-link> |
      <router-link to="/5">LOGOUT</router-link>
    </div>
    <div id="second-nav">
      <router-link to="/profile">NickName</router-link> |
      <router-link to="/store">Coins</router-link> |
      <router-link to="/close">Close</router-link>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Layout',
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#main-nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
