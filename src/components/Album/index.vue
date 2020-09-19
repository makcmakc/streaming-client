<template>
  <div class="album-container">
    <album-item class="album-container__item" />
    <album-item class="album-container__item" />
    <album-item class="album-container__item" />
  </div>
</template>


<script>
  import AlbumItem from './AlbumItem'
  export default {
    name: 'album-container',
    components: {
      AlbumItem
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
    width: 20%;
    padding: 10px;
    vertical-align: top;
  }
}  
</style>
