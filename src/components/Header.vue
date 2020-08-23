<template>
  <div class="header" :style="style">
      <slot></slot>
  </div>
</template>

<script>
export default {
    props: ["bg"],
    computed: {
        style() {
            return 'background-color: ' + this.bg;
        }
    }
}
</script>

<style>

</style>