<template>
  <div id="app">
    <Menu class="menu"></Menu>
    <div class="router">
      <router-view/>
    </div>
  </div>
</template>
<script>
import Menu from "./components/Menu";
export default {
  data() {
    return {
      bgImg: "green"
    }
  },
  components: {
    Menu
  },
  mounted() {
    this.changeBg(this.$route.name === "Home" ? true : false);
  },
  methods: {
    changeBg(isHome) {
      this.bgImg = isHome ? "green" : "red";
    }
  }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* background-image: ; */
  /* background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('./assets/sss2.jpg');
  background-repeat: no-repeat;
  background-size: cover; */
  text-align: center;
  /* display: flex; */
  color: #fff;
  height: 100%;
}

#app .menu {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('./assets/sss2.jpg');
  background-repeat: no-repeat;
  background-size: cover;
}

/* #app .router {
  background-color: #202F2B;
} */

body {
  margin: 0;
  height: 100%;
  background-color: #0d0e0af5;
  /* background-image: url('./assets/bgbg.jpg');
  background-repeat: no-repeat;
  background-size: cover; */
}

html {
  height: 100%
}
</style>
