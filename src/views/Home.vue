<template>
  <div class="home">
    <div class="description">
      <h2>About Me</h2>
      <div>Description</div>
    </div>
    <div class="avatar">
      <picture>
        <source srcset="../assets/rsz_small_background2.jpg" media="(max-width: 768px)"/>
        <source srcset="../assets/rsz_background2.jpg" />
        <img srcset="../assets/rsz_background2.jpg" />
      </picture>
    </div>   
  </div>
</template>

<script>

export default {
  name: 'Home',
  components: {
  }
}
</script>
<style scoped>
.home {
  display: flex;
  height: 100%;
  flex-direction: row;
  justify-content: center;
  padding: 3rem;
}

.description h2 {
  padding-top: 5npm run serve
  0px;
}

.home div {
  flex: 1
}

.background {
  background-image: url('../assets/bg2.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  height: 100%;
}

@media screen and (max-width: 768px) {
  .home {
    flex-direction: column-reverse;
  }

  .description h2 {
    padding-top: 10px;
  }
}

</style>