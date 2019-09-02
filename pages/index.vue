<template>
  <div>
    <div class="flex flex-col items-center justify-between h-screen" :class="'bg-' + this.color + '-300'">
      <nav-bar :color="color" />
      <div class="rounded shadow-lg p-6" :class="'bg-' + this.color + '-200'">
        <div class="container has-text-centered">
          <div class="player has-text-centered" :style="'--player-height: ' + height + 'px; --player-width: ' + width + 'px'">
            <youtube :player-width="width" :player-height="height" :video-id="videoId" :player-vars="playerVars" :mute="true" @ready="ready" @playing="playing"></youtube>
          </div>
        </div>
      </div>
    <div/>
    </div>
  </div>  
</template>

<script>
import NavBar from "~/components/NavBar.vue";
export default {
  components: {
    NavBar
  },
  data() {
    let colors = ["gray", "red", "orange", "yellow", "green", "teal", "blue", "indigo", "purple", "pink"];
    let colorIndex = Math.floor(Math.random() * colors.length);
    return {
      videoId: '0JvG551iDTE',
      width: window.screen.width/2,
      height: 0.625*(window.screen.width/2),
      color: colors[colorIndex],
      playerVars: {
        autoplay: 1,
      }
    }
  },
  methods: {
    ready (event) {
      this.player = event.target
    },
    playing (event) {
      // The player is playing a video.
    },
    change () {
      // when you change the value, the player will also change.
      // If you would like to change `playerVars`, please change it before you change `videoId`.
      // If `playerVars.autoplay` is 1, `loadVideoById` will be called.
      // If `playerVars.autoplay` is 0, `cueVideoById` will be called.
      this.videoId = 'another video id'
    },
    stop () {
      this.player.stopVideo()
    },
    pause () {
      this.player.pauseVideo()
    }
  }
}
</script>

<style>
iframe {
  height: var(--player-height);
  width: var(--player-width);
}
</style>
