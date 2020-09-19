<template>
  <div class="volume-bar">
    <div class="volume-bar__button">
      <i class="material-icons">volume_up</i>
    </div>
    <vue-slider 
      class="volume-bar__slider"
      v-model="volume"
      :dot-size="20"
      :process-style="{ backgroundColor: '#1db954' }"
      width="120px"
      height="6px"
    ></vue-slider>
  </div>
</template>

<script>
  import VueSlider from 'vue-slider-component'
  import 'vue-slider-component/theme/antd.css'
  export default {
    name: "volume-bar",
    data() {
      return {
        volume: 50,
      };
    },    
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
    margin-top: -4px;
  }
}
</style>
