<template>
  <div class="album-item">
    <div class="album-item__cover">
      <img
        v-if="album.coverImg"
        class="album-item__cover-inner"
        :src="album.coverImg"
        :alt="album.coverImg + '-cover'"
      />

      <div v-else class="album-item__cover-inner">
        <i class="material-icons album-item__music-icon">audiotrack</i>
      </div>

      <div class="album-item__cover-hover">

        <div class="album-item__play">
          <i class="material-icons">play_arrow</i>
        </div>

        <div class="album-item__sound-on">
          <i class="material-icons">audiotrack</i>
        </div>
        
        <div class="album-item__pause">
          <i class="material-icons">pause</i>
        </div>
        

      </div>
    </div>

    <div class="album-item__info">
      <a href="#" class="album-item__name">{{ album.name }}</a>
      <a href="#" class="album-item__artist">{{ album.artists }}</a>
    </div>   
  </div>
</template>


<script>

  export default {
    name: 'album-item',
    props: {
      album: {
        // id: {
        //   required: true
        // },
        // uri: {
        //   required: true
        // },
        // coverImg: {
        //   required: true
        // },
        // name: {
        //   type: String,
        //   required: true
        // },
        // type: {
        //   required: true
        // },
        // artists: {
        //   required: false
        // }  
      }      
    },    
    // data: () => ({
    //   simpleValue: 50,
    //   albumName: "(What's The Story) Mornig Glory?",
    //   albumArtist: "Oasis",
    //   coverImg: "https://upload.wikimedia.org/wikipedia/ru/2/25/Uk_whats_the_story_lg.jpg"
    // }),
    components: {

    },
    mounted() {
      console.log(this.album)
    }
  }
</script>


<style lang="scss">

.album-item:hover .album-item__play i {
  display: block;
}

.album-item--active .album-item__name {
  color: #1db954;
}



.album-item--playing {
  .album-item__sound-on {
    display: block;
  }

  &:hover {
    .album-item__pause {
      display: block;
    }

    .album-item__play, .album-item__sound-on {
      display: none;
    }
  }
}

.album-item__pause , .album-item__sound-on {
  display: none;
}

.album-item__play i, .album-item__pause i {
  font-size: 50px;
}

.album-item__sound-on i {
  position: relative;
  width: 60px;
  height: 60px;
  background: rgba(0, 0, 0, 0.6);
  border-radius: 50%;
  font-size: 40px;
  padding-left: 8px;
  padding-top: 10px;
}

.album-item__play i {
  display: none;
}

.album-item {
  &__cover {
    position: relative;
    min-width: 130px;
    padding-top: 100%;
    &:hover .album-item__cover-hover {
      background: rgba(0, 0, 0, 0.6);
    }
    &-inner {
      position: absolute;
      top: 0;
      height: 100%;
      width: 100%;
      background: #959595;
    }
    &-hover {
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
  }

  &__info {
    margin-top: 8px;
    font-size: 14px;
    line-height: 28px;

    display: flex;
    flex-direction: column;
  }
  &__name {
    color: #fff;
    cursor: pointer;
    font-size: 18px;

    &:hover {
      text-decoration: underline;
    }
  }

  &__artist {
    color: #959595;
    text-decoration: none;
    font-size: 16px;

    &:hover {
      color: #fff;
      text-decoration: underline;
    }
  }

  &__avatar {
    position: relative;
    min-width: 130px;
    min-height: 130px;
    width: 100%;
    height: 100%;
    background: #737575;
  }

  &__music-icon {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 100px; 
  }    
}

</style>
