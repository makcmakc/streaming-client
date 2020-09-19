<template>
  <div class="navbar-nav">
    <div class="navbar-nav__item">
      <a class="navbar-nav__link">Maximillian</a>
      <button class="navbar-nav__icon" @click="onClick">
        <i class="material-icons">keyboard_arrow_down</i>
      </button>
    </div>
    <transition name="fade">
      <ul class="navbar-nav__dropdown" v-show="isVisible">
        <li class="navbar-nav__list-item">Account</li>
        <li class="navbar-nav__list-item">Help</li>
        <li class="navbar-nav__list-item">Logout</li>
      </ul>
    </transition>
  </div>
</template>

<script>
  export default {
    name: 'navbar-nav',
    data() {
      return {
        isVisible: false
      }
    },
    methods: {
      clickOutEvent(event) {
        const $dropdown = this.$el.children[0]
        if (event.target !== $dropdown && !$dropdown.contains(event.target)) {
          this.close()
        }
      },
      onClick() {
        this.isVisible = !this.isVisible

        if (this.isVisible) {
          setTimeout(() => document.addEventListener("click", this.clickOutEvent), 100)
        } else {
          this.close()
        }
      },

      close() {
        this.isVisible = false
        document.removeEventListener("click", this.clickOutEvent)
      },      
    }
  };
</script>

<style scoped lang="scss">
.navbar-nav {
  position: relative;
  z-index: 10;
  &__item {
    display: flex;
    align-items: center;
    height: 42px;
  }
  &__link {
    color: #fff;
    font-size: 13px;

    &:hover {
      text-decoration: underline;
    }
  }
  &__icon {
    margin: 0 6px;
    color: #fff;
    line-height: 0;
    outline: none;
    cursor: pointer;
    i {
      font-size: 18px;
      margin-top: 4px;
    }
  }
  &__dropdown {
    font-size: 13px;
    font-weight: normal;
    background: #404040;
    box-shadow: -2px 2px 5px 0 rgba(0, 0, 0, 0.75);
  }
  &__list-item {
    padding: 10px;
    cursor: pointer;
    // think about it
    color: rgba(255, 255, 255, .8);
    
    &:hover {
      background: #2f2f2f;
    }
  }
  .fade-enter-active, .fade-leave-active {
    transition: opacity 0.3s;
  }

  .fade-enter, .fade-leave-to {
    opacity: 0;
  }  
}
</style>
