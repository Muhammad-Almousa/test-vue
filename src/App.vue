<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">LILLYDOO</router-link>
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
@font-face {
  font-family: "museo";
  src: local("museo"), local("museo"),
    url("assets/fonts/Museo-300.woff2") format("woff2");
}
@font-face {
  font-family: "cera_medium";
  src: local("cera_medium"), local("cera_medium"),
    url("assets/fonts/CeraPro-Medium.woff") format("woff");
}
@font-face {
  font-family: "cera_regular";
  src: local("cera_regular"), local("cera_regular"),
    url("assets/fonts/CeraPro-Regular.woff") format("woff");
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

// Break-points
// $breakpoint-xs: 575.98px;
// $breakpoint-md: 767.98px;
// $breakpoint-l: 1024px;
// $breakpoint-xl: 1199.98px;

#app {
  font-family: "cera_regular";
  color: #2c3e50;
}
#nav {
  padding: 20px;
  background: #fff;
  a {
    font-family: museo, Arial, Helvetica, sans-serif;
    font-size: 2rem;
    color: #2c3e50;
  }
}

h1 {
  font-family: museo, Arial, Helvetica, sans-serif;
  font-size: 2.5rem;
  line-height: 2.5rem;
  font-weight: 300;
  color: #000;
}

h2 {
  margin: 15px auto 30px auto;
  font-family: cera_medium, Arial, Helvetica, sans-serif;
  font-size: 1.7rem;
  line-height: 1.8rem;
  font-weight: normal;
  color: #000;
}

h3 {
  margin: 15px auto;
  font-family: cera_medium, Arial, Helvetica, sans-serif;
  font-size: 1.1rem;
  line-height: 1.2rem;
  font-weight: 300;
  color: #000;
}

section {
  display: flex;
  flex-flow: row wrap;
  align-items: center;
  position: relative;
  min-height: 450px;
  padding: 2vw 0;
}

.row {
  display: flex;
  flex-flow: row;
  align-items: center;
  position: relative;
  width: 80vw;
  max-width: 1280px;
  margin: 0 auto;
  padding: 3vw 2vw;
}

a {
  text-decoration: none;
}

.btn {
  padding: 12px 20px;
  background: #00afab;
  color: #fff;
}
</style>
