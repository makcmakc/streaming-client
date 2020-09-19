<template>
  <div class="albums-view">
    <entity-header title="Albums" />

    <div class="albums-view__content">
      <album />
    </div>

  </div>
</template>

<script>
  import EntityHeader from "@/components/EntityHeader"
  import Album from "@/components/Album"
  export default {
    name: 'albums',
    data: () => ({
      id: 1,
      uri: "string",
      coverImg: "https://upload.wikimedia.org/wikipedia/ru/2/25/Uk_whats_the_story_lg.jpg",
      name: "Morning Glory",
      type: "",
      artists: "Oasis"
    }),    
    components: {
      EntityHeader,
      Album
    }
  }
</script>

<style lang="scss">
.albums-view {
  &__content {

  }
}
</style>