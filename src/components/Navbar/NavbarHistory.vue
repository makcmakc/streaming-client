<template>
  <div class="navbar-history">
    <a class="navbar-history__link" @click="onPrevClick">
      <i class="material-icons">keyboard_arrow_left</i>
    </a>
    <a class="navbar-history__link" @click="onNextClick">
      <i class="material-icons">keyboard_arrow_right</i>
    </a>
  </div>
</template>

<script>
  export default {
    name: "navbar-history",
    methods: {
      onNextClick() {
        console.log('Next')
      },

      onPrevClick() {
        console.log('Back')
      }
    }
  };
</script>

<style scoped lang="scss">
.navbar-history {
  display: inline-block;
  &__link {
    margin: auto 5px;
    line-height: 0;
    cursor: pointer;
    i {
      color: #fff;
    }
  }
}
</style>
