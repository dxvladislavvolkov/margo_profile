<template>
  <div class="photo-container">
    <div class="photo-preview">
      <img @mouseover="showDescr" @mouseleave="hideDescr"  :src="require('../assets/images/' + photo.preview)" @click="onClick" />
    </div>
    <div>
      {{photo.name}}
    </div>
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
            this.$emit('onClick', { image: this.$vnode.componentOptions.propsData.photo, index: this.$vnode.key });
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

}

.photo-preview {
  width: 322px;
  padding: 30px 20px 10px;
}

/* img:hover {
    opacity: .5;
    transition: .9s;
    transform: scale(1.04);
} */
.description {
    margin-top: -70px;
    padding: 10px;
    background-color: rgb(255, 255, 255, 0.7);
}
/* .decs-enter-active {
  transition: all .3s ease;
}
.decs-leave-active {
  transition: all .3s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.decs-enter, .decs-leave-to {
  transform: translateY(20px);
  opacity: 0;
} */
</style>