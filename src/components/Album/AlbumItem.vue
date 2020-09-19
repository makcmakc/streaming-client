<template>
  <div class="album-item">


    <div class="media-object">

    <div class="media-object__cover">
      <img
        v-if="coverImg"
        class="media-object__cover-inner"
        :src="coverImg"
        :alt="coverImg + '-cover'"
      />

      <div v-else class="media-object__cover-inner">
        <i class="material-icons media-object__music-icon">audiotrack</i>
      </div>

      <div class="media-object__cover-hover">

        <div class="media-object__play">
          <i class="material-icons">play_arrow</i>
        </div>

        <div class="media-object__sound-on">
          <i class="material-icons">audiotrack</i>
        </div>
        
        <div class="media-object__pause">
          <i class="material-icons">pause</i>
        </div>
        

      </div>
    </div>

    <modal name="my-first-modal">
        This is my first modal
    </modal>
    
    <div class="media-object__info">
      <a href="#" class="media-object__name">{{ albumName }}</a>
      <a href="#" class="media-object__artist">{{ albumArtist }}</a>
    </div>   
</div>
  </div>
</template>


<script>

  export default {
    name: 'album-item',
    data: () => ({
      simpleValue: 50,
      albumName: "(What's The Story) Mornig Glory?",
      albumArtist: "Oasis",
      coverImg: "https://upload.wikimedia.org/wikipedia/ru/2/25/Uk_whats_the_story_lg.jpg"
    }),
    components: {

    },
    methods: {
        show () {
            this.$modal.show('my-first-modal');
        },
        hide () {
            this.$modal.hide('my-first-modal');
        }
    },
  }
</script>


<style lang="scss">

.media-object:hover .media-object__play i {
  display: block;
}

.media-object--active .media-object__name {
  color: #1db954;
}



.media-object--playing {
  .media-object__sound-on {
    display: block;
  }

  &:hover {
    .media-object__pause {
      display: block;
    }

    .media-object__play, .media-object__sound-on {
      display: none;
    }
  }
}

.media-object__pause , .media-object__sound-on {
  display: none;
}

.media-object__play i, .media-object__pause i {
  font-size: 50px;
}

.media-object__sound-on i {
  position: relative;
  width: 60px;
  height: 60px;
  background: rgba(0, 0, 0, 0.6);
  border-radius: 50%;
  font-size: 40px;
  padding-left: 8px;
  padding-top: 10px;
}

.media-object__play i {
  display: none;
}

.media-object__cover {
  position: relative;
  min-width: 130px;
  padding-top: 100%;

  &:hover .media-object__cover-hover {
    background: rgba(0, 0, 0, 0.6);
  }
}

.media-object__cover-inner {
  position: absolute;
  top: 0;
  height: 100%;
  width: 100%;
  background: #959595;
}

.media-object__cover-hover {
  display: block;
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;

  i {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: #fff;
    outline: none;
  }
}

.media-object__info {
  margin-top: 5px;
  font-size: 14px;
  line-height: 20px;

  display: flex;
  flex-direction: column;
}

.media-object__name {
  color: #fff;
  cursor: pointer;

  &:hover {
    text-decoration: underline;
  }
}

.media-object__artist {
  color: #959595;
  text-decoration: none;

  &:hover {
    color: #fff;
    text-decoration: underline;
  }
}

.media-object__avatar {
  position: relative;
  min-width: 130px;
  min-height: 130px;
  width: 100%;
  height: 100%;
  background: #737575;
}

.media-object__music-icon {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 100px; 
}    
</style>
