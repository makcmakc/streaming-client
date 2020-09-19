<template>
  <form class="navbar-search">
    <input
      class="navbar-search__input"
      type="search"
      placeholder="Search"
      aria-label="Search"
    />
    <button class="navbar-search__btn">
      <i class="material-icons">search</i>
    </button>
  </form>
</template>

<script>
  export default {
    name: "navbar-search",
  };
</script>

<style scoped lang="scss">
.navbar-search {
  position: relative;
  width: 160px;
  font-size: 14px;
  &__input {
    height: 25px;
    margin: 0;
    padding-right: 20px;
    border-radius: 30px;
  }
  &__btn {
    position: absolute;
    right: 6px;
    top: 0;
    bottom: 0;
    height: 16px;
    margin: auto 0;
    color: #242729;
    outline: none;
    pointer-events: none;
    i {
      margin-top: -1px;
      font-size: 18px;
    }
  }
}
</style>
