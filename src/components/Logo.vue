<template>
  <span @click="goToDefault" class="main-logo">I'M MARGO</span>
</template>

<script>
export default {
  methods: {
    goToDefault() {
      this.$router.push({ path: '/' });
    }
  }
}
</script>

<style scoped>
.main-logo {
  cursor: pointer;
}
</style>