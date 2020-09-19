<template>
  <div class="current-track">
    <div class="current-track__cover">
      <a href="#">
      <img
        class="current-track__img"
        src="https://upload.wikimedia.org/wikipedia/ru/2/25/Uk_whats_the_story_lg.jpg"
      />
      </a>
    </div>
    <div class="current-track__info">
      <a href="#" class="current-track__name">Wonderwall</a>
      <div class="current-track__artists">
        <a href="#" class="current-track__link">Oasis</a>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "current-track"
  };
</script>

<style lang="scss">
.current-track {
  display: flex;
  align-items: center;
}
.current-track__cover {
  width: 56px;
  min-width: 56px;
  height: 56px;
  margin: 0 15px;
}
.current-track__img {
  width: 100%;
}
.current-track__info {
  position: relative;
  overflow: hidden;
  padding-right: 20px;
  white-space: nowrap;
  text-overflow: ellipsis;
}
.current-track__info .track-addition {
  position: absolute;
  right: 0;
  top: 2px;
}
.current-track__name {
  color: #fff;
  font-size: 14px;
}
.current-track__name:hover {
  text-decoration: underline;
}
.current-track__artists {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  padding: 5px 0;
  font-size: 11px;
}
.current-track__link {
  color: #959595;
}
.current-track__link:hover {
  color: #fff;
  text-decoration: underline;
}
</style>
