<template>
  <div class="sidebar-nav">
    <h2 v-if="title" class="sidebar-nav__title">
      {{ title }}
    </h2>
    <ul>
      <li class="sidebar-nav__item">
        <i class="material-icons sidebar-nav__playing-icon"></i>
      </li>         
    </ul>
  </div>
</template>

<script>

  export default {
    name: "sidebar-nav",
    props: {
      title: {
        type: String,
        required: false
      }
    },
  };
</script>

<style scoped lang="scss">
.sidebar-nav {
  padding-right: 10px;
  color: #959595;
  font-size: 14px;

  &__title {
    padding-left: 23px;
    font-size: 12px;
    font-weight: normal;
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  &__item {
    position: relative;
    margin-bottom: 10px;
    padding-left: 23px;
    padding-right: 20px;
    cursor: pointer;
    &:hover {
      color: #fff;
    }
    &--active {
      color: #fff;
      &:before {
        position: absolute;
        left: 0;
        height: 100%;
        border-left: 4px solid #1db954;
        content: "";
      }
    }
  }
}

.sidebar-nav__playing-icon {
  position: absolute;
  right: 3px;
  top: 0;
  color: #fff;
  outline: none;
}
</style>
