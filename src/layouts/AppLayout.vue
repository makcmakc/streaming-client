<template>
  <div class="app-layout">
    <navbar />
    <div class="app-layout__wrap">
      <sidebar />
      <div class="app-layout__main">
        <router-view />
      </div>
      <player />
    </div>
  </div>
</template>

<script>
  import Navbar from "@/components/Navbar"
  import Sidebar from "@/components/Sidebar"
  import Player from "@/components/Player"

  export default {
    name: "AppLayout",
    components: {
      Navbar,
      Sidebar,
      Player
    }
  };
</script>

<style scoped lang="scss">
.app-layout {
  position: relative;
  display: flex;
  flex-flow: column;
  flex-grow: 1;
}

.app-layout__wrap {
  display: flex;
  flex-flow: row;
  flex-grow: 1;
}

.app-layout__main {
  flex-grow: 1;
  max-height: calc(100vh - 130px);
  overflow-y: auto;
}

.app-layout .sidebar {
  width: 220px;
  min-width: 220px;
}
</style>
