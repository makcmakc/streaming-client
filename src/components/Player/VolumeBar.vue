<template>
  <div class="volume-bar">
    <div class="volume-bar__button">
      <i class="material-icons">volume_up</i>
    </div>
    <vue-slider 
      width="100px"
      height="8px"
    />
  </div>
</template>

<script>
  import VueSlider from 'vue-slider-component'
  import 'vue-slider-component/theme/antd.css'
  export default {
    name: "volume-bar",
    components: {
      VueSlider
    }
  };
</script>

<style lang="scss">
.volume-bar {
  display: flex;
  align-items: center;

  &__button {
    margin-right: 15px;
    color: #959595;
    cursor: pointer;
    outline: none;
    &:hover {
      color: #fff;
    }
  }
  &__slider {
    width: 100px;
    height: 8px;
    background: #1db954;
    margin-top: -4px;
    border-radius: 10px;
  }
}
</style>
