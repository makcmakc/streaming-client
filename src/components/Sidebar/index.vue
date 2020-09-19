<template>
  <div class="sidebar">
    <div class="sidebar__inner">
      <sidebar-nav :links="browse" />
      <sidebar-nav title="Library" :links="library" />
      <sidebar-nav title="Playlists" />
      <sidebar-nav title="Albums" />
    </div>
    <button class="sidebar__btn">
      <span>New playlist</span>
      <i class="material-icons sidebar__btn-icon">add</i>
    </button>
  </div>
</template>

<script>
import SidebarNav from "./SidebarNav"

  export default {
    name: "sidebar",
    data: () => ({

    }),
    components: {
      SidebarNav
    },
    computed: {
      browse() {
        return [
          {
            type: "browse",
            name: "Browse"
          }
        ];
      },

      library() {
        return [
          {
            type: "tracks-collection",
            name: "Songs"
          },
          {
            type: "albums-collection",
            name: "Albums"
          },
          {
            type: "artists-collection",
            name: "Artists"
          }
        ];
      }      
    }
  };
</script>

<style scoped lang="scss">
  .sidebar {
    position: relative;
    padding-top: 30px;
    background: #181818;

    &__inner {
      max-height: calc(100vh - 232px);
    }

    &__btn {
      display: flex;
      align-items: center;
      position: absolute;
      bottom: 90px;
      height: 50px;
      width: 100%;
      margin-top: 20px;
      padding: 0 15px;
      color: #959595;
      font-size: 14px;
      border-top: 1px solid #737575;
      outline: 0;
      cursor: pointer;
      &-icon {
        margin: auto 8px;
      }

      &:hover {
        color: #fff;
      }
    }

    .sidebar-nav {
      &:not(:last-of-type) {
        margin-bottom: 30px;
      }
    }
  }
</style>
