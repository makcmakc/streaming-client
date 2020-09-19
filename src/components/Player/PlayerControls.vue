<template>
  <div class="player-controls">
    <div  class="player-controls__button" title="Shuffle">
      <i class="material-icons">shuffle</i>
    </div>


    <div class="player-controls__button icon-previous" title="Previous">
      <i class="material-icons">skip_previous</i>
    </div>

    <div>
      <i class="player-controls__button player-controls__button--play material-icons">play_arrow</i>
    </div>

    <div class="player-controls__button icon-next" title="Next">
      <i class="material-icons">skip_next</i>
    </div>

    <div class="player-controls__button" title="Repeat">
      <i class="material-icons">loop</i>
    </div>
  </div>
</template>

<script>

  export default {
    name: "player-controls",
  };
</script>

<style scoped lang="scss">

.player-controls {
  display: flex;
  justify-content: center;

  &__button {
    margin: auto 10px;
    color: #959595;
    font-size: 15px;
    cursor: pointer;
    outline: none;

    &:hover {
      color: #fff;
    }

    &--active {
      color: #1db954;
    }

    &--play,
    &--pause {
      font-size: 35px;
      &:hover {
        color: #fff;
        transform: scale(1.1);
      }
    }
  }
}
</style>
