<template>
  <nav class="navbar">
    <navbar-history />
    <navbar-search />
    <navbar-nav />
  </nav>
</template>

<script>
  import NavbarHistory from "./NavbarHistory"
  import NavbarSearch from "./NavbarSearch"
  import NavbarNav from "./NavbarNav"

  export default {
    name: "navbar",

    components: {
      NavbarHistory,
      NavbarSearch,
      NavbarNav
    }
  };
</script>

<style scoped lang="scss">
.navbar {
  display: flex;
  height: 42px;
  background: #242729;

  .navbar-history {
    display: flex;
    margin-left: 6px;
  }
  .navbar-search {
    display: flex;
    align-items: center;
    margin-left: 6px;
  }
  .navbar-nav {
    margin: auto 30px auto auto;
  }
}
</style>
