<template>
  <nav>
    <router-link to="/">Home</router-link>
    <router-link to="/about">About</router-link>
  </nav>
  <router-view />
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: $color-light;
  background-color: $background-light;
  height: 100vh;
  width: 100vw;
}

body {
  padding: 0;
  margin: 0;
}

nav {
  padding: 20px;
  background-color: $nav-bg-light;

  a {
    font-weight: bold;
    text-decoration: none;
    padding: 10px;
    transition: all 0.3s ease-in-out;
    margin-right: 5px;
    color: $nav-active-light;

    &:hover {
      background-color: $nav-bg-dark;
      color: $color-dark;
    }

    &.router-link-exact-active {
      border: 1px solid $nav-active-light;
    }
  }
}
</style>
