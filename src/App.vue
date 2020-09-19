<template>
  <div id="app" class="app">
    <app-layout />
  </div>
</template>

<script>
  import AppLayout from "@/layouts/AppLayout"
  export default {
    name: "app",
    components: {
      AppLayout
    }
  };
</script>

<style lang="scss">
@import "styles/index";
.app {
  display: flex;
  flex-flow: column;
  position: absolute;
  width: 100%;
  min-width: 630px;
  height: 100%;
  background: $c-mine-shaft;
}
</style>
