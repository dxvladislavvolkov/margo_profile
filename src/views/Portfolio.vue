<template>
  <div class="portfolio">
    <Popup v-if="showPopup">
      <img class="full-img" :src="imgUrl" />
    </Popup>
    <div class="gallary-container">
        <Preview class="photo" v-for="(image, index) in images" :key="index" :photo="image" @onClick="openFullAlbum" />
    </div>
  </div>
</template>

<script>
import Preview from "../components/PhotoPrewiew";
import Popup from "../components/Popup"
const images = [{
  preview: '6.jpg',
  name: 'Name 1',
  photos: ["6.jpg", "6.jpg", "6.jpg"],
  id: '1'
}, {
  preview: '6.jpg',
  name: 'Name 2',
  photos: ["6.jpg", "6.jpg", "6.jpg"],
  id: '2'
}, {
  preview: '6.jpg',
  name: 'Name 3',
  photos: ["6.jpg", "6.jpg"],
  id: '3'
}, {
  preview: '6.jpg',
  name: 'Name 1',
  id: '1'
}, {
  preview: '6.jpg',
  name: 'Name 1',
  id: '1'
}, {
  preview: '6.jpg',
  name: 'Name 1',
  id: '1'
}, {
  preview: '6.jpg',
  name: 'Name 1',
  id: '1'
}]
export default {
  data() {
    return {
      images,
      listImages: null,
      selectedImage: "",
      showPopup: false
    }
  },
  components: {
    Preview,
    Popup
  },
  computed: {
    imgUrl() {
      /* eslint-disable no-debugger */
            debugger;
      return this.listImages('./' + this.selectedImage);
    }
  },
  mounted() {
    this.listImages = require.context('../assets/images/', false, /\.jpg$/)
  },
  methods: {
    openFullAlbum(e) {
      /* eslint-disable no-debugger */
      this.$router.push({ path: `/album/${e.index}` });
      // this.selectedImage = e.image;
      // this.showPopup = true;
    }
  }

}
</script>

<style>
.portfolio {
  text-align: center;
  padding: 40px;
}
.gallary-container {
  display: flex;
  flex-direction: row;
  flex-flow: row wrap;
  flex-wrap: wrap;
  justify-content: space-evenly;
}


.full-img {
  width: 100%;
}

.photo img {
  width: 100%;
  height: auto;
}
</style>