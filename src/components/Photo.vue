<template>
  <div class="photo-container">
    <figure class="photo">
      <img @mouseover="showDescr" @mouseleave="hideDescr"  :src="require('../assets/images/1/' + photo)" @click="onClick" />
    </figure>
  </div>
</template>

<script>
export default {
    props: ["photo"],
    data() {
        return {
            show: true
        }
    },
    methods: {
        onClick() {
            // this.$emit('onClick', { image: this.$vnode.componentOptions.propsData.photo, index: this.$vnode.componentOptions.propsData.photo.id });
        },
        showDescr() {
            this.show = true;
        },
        hideDescr() {
            this.show = true;
        }
    }
}
</script>

<style scoped>
img {
  cursor: pointer;
  width: 100%;
  height: auto;
}

.photo {
  margin: 20px;
}

.photo-container {
    flex: auto;
    width: 200px;
}

@media screen and (max-width: 768px) {
  .photo-container {
    width: 100%;
  }
}

</style>