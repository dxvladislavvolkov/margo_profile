<template>
  <div class="album">
      <photo v-for="(photo, index) in photos" :key=index :photo="photo" />
  </div>
</template>

<script>
import Photo from "../components/Photo";
export default {
    components: {
        Photo
    },
    data() {
        return {
            photos: [
                "5.jpg",
                "6.jpg",
                "1.jpg",
                "5.jpg",
                "6.jpg",
                "1.jpg"
            ]
        }
    }
}
</script>

<style scoped>
.album {
    max-width: 768px;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    flex-wrap: wrap;
    margin: 0 auto;
}

@media screen and (max-width: 768px) {
  .album {
    flex-direction: column;
  }
}

</style>