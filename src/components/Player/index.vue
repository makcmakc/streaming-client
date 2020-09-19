<template>
  <div class="player">
    <div class="player__inner">
      <current-track class="player__left" />

      <div class="player__center">
        <player-controls />
      </div>

      <div class="player__right">
        <volume-bar />
      </div>
    </div>
  </div>
</template>

<script>
  import VolumeBar from "./VolumeBar"
  import CurrentTrack from "./CurrentTrack"
  import PlayerControls from "./PlayerControls"

  export default {
    name: "player",
    components: {
      VolumeBar,
      CurrentTrack,
      PlayerControls
    },
  };
</script>

<style scoped lang="scss">
.player {
  position: fixed;
  bottom: 0;
  width: 100%;
  height: 90px;
  z-index: 2;
  background: #242729;
  &__inner {
    display: flex;
    align-items: center;
    height: 100%;
  }
  &__left {
    width: 30%;
    min-width: 180px;
  }
  &__right {
    display: flex;
    width: 30%;
    min-width: 180px;
    .device-picker {
      margin: 2px 5px 0 auto;
    }
    .volume-bar {
      margin: 0 15px 0 5px;
    }
  }
  &__center {
    width: 60%;
  }
}
</style>
