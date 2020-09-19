<template>
  <div class="album-container">
    <album-item  v-for="album in albums" :key="album.id" :album="album" class="album-container__item" />
  </div>
</template>


<script>
  import AlbumItem from './AlbumItem'
  export default {
    name: 'album-container',
    components: {
      AlbumItem
    },
    data() {
      return {
        albums: [
          {
            id: 1,
            uri: "sadsa",
            coverImg: "https://upload.wikimedia.org/wikipedia/ru/2/25/Uk_whats_the_story_lg.jpg",
            name: "(What's The Story) Mornig Glory?",
            type: "Brit Rock",
            artists: "Oasis"
          },
          {
            id: 2,
            uri: "asdsa",
            coverImg: "https://upload.wikimedia.org/wikipedia/ru/4/44/SmashingPumpkins-SiameseDream.jpg",
            name: "Siamese Dream",
            type: "Rock",
            artists: "The Smashing Pumpkins"
          },
          {
            id: 3,
            uri: "sadas",
            coverImg: "https://upload.wikimedia.org/wikipedia/ru/0/0f/Museoosalbcov.jpg",
            name: "Origin of Symmetry",
            type: "Rock",
            artists: "Muse"
          }                
        ]        
      }
    }
  }
</script>


<style lang="scss">
.album-container {
  display: flex;
  flex-flow: wrap;
  padding: 0 10px;
  &__item {
    display: inline-block;
    width: 18%;
    padding: 10px;
    vertical-align: top;
  }
}  
</style>
