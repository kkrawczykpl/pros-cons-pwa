<template>
  <!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav> -->
  <router-view />
</template>

<style lang="scss">
:root {
  --black: #000000;
  --white: #ffffff;
  --background-light: #f9fafe;
  --pros-light: #4355fe;
  --cons-light: #f38da3;
  --grey: #eee;
}

*,
*:before,
*:after {
  box-sizing: inherit;
}

html,
body {
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
}

html {
  max-width: 70ch;
  margin: auto;
  line-height: 1.75;
  font-size: 1.25em;
  background-color: var(--background-light);
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
