<template>
    <div class="menu-container">
        <Logo />
        <div id="nav">
            <router-link to="/">About</router-link>
            <router-link to="/portfolio">Portfolio</router-link>
            <router-link to="/contact">Contacts</router-link>
        </div>
    </div>
</template>

<script>
import Logo from './Logo';
export default {
    components: {
        Logo
    }
}
</script>

<style>
#nav {
  /* padding: 55px;
  text-align: start; */
  display: flex;
  flex-direction: row;
  justify-content: center;
  width: 25%;
  padding-top: 10px;
  margin: 0 auto;
}

.menu-container {
    padding-top: 10%;
}

.menu-container .main-logo {
    /* width: 15%; */
    padding-top: 10%;
    margin-block-start: 0;
    font-size: 24px;
    border-bottom: 1px solid #fff;
}

#nav a {
  font-weight: bold;
  color: #fff;
  flex: 1;
}

#nav a {
  padding: 5px 10px;
  margin: 10px;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: #1fb4cc;
  border-radius: 10%;
}
</style>