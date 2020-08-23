<template>
  <div class="popup" >
      <div>close</div>
      <div class="content">
          <slot></slot>
      </div>
  </div>
</template>

<script>
export default {
    el: "#modal"
}
</script>

<style scoped>
.popup {
    position: absolute;
    width: 100%;
    height: auto;
    z-index: 10001;
}

.content {
    width: 50%;
}

</style>