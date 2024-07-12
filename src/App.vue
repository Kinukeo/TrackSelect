<script setup>
import TrackIcon from './components/TrackIcon.vue'
import blizzardBluff from './assets/TrackPreviews/blizzard-bluff.jpg'
import cocoPark from './assets/TrackPreviews/coco-park.jpg'
import cortexCastle from './assets/TrackPreviews/cortex-castle.jpg'
import crashCove from './assets/TrackPreviews/crash-cove.jpg'
import dingosCanyon from './assets/TrackPreviews/dingo-s-canyon.jpg'
import dragonMines from './assets/TrackPreviews/dragon-mines.jpg'
import hotairSkyway from './assets/TrackPreviews/hot-air-skyway.jpg'
import mysteryCaves from './assets/TrackPreviews/mystery-caves.jpg'

const tracks = [
  { trackName: 'Blizzard Bluff', imageSrc: blizzardBluff },
  { trackName: 'Coco Park', imageSrc: cocoPark },
  { trackName: 'Cortex Castle', imageSrc: cortexCastle },
  { trackName: 'Crash Cove', imageSrc: crashCove },
  { trackName: "Dingo's Canyon", imageSrc: dingosCanyon },
  { trackName: 'Dragon Mines', imageSrc: dragonMines },
  { trackName: 'Hot Air Skyway', imageSrc: hotairSkyway },
  { trackName: 'Mystery Caves', imageSrc: mysteryCaves }
]
</script>

<template>
  <main>
    <div class="container">
      <header style="color: #ed6802; font-size: 40px">Track Select</header>
      <div class="player-container">
        <div class="player">
          <div class="player-name">Player One</div>
          <div class="player-square"></div>
        </div>
        <div class="player">
          <div class="player-name">Player Two</div>
          <div class="player-circle"></div>
        </div>
      </div>
    </div>
    <div class="track-icons-container">
      <div class="track-icons">
        <TrackIcon
          v-for="track in tracks"
          :key="track.trackName"
          :imageSrc="track.imageSrc"
          :trackName="track.trackName"
        />
      </div>
    </div>
  </main>
</template>

<style scoped>
.container {
  display: flex;
  justify-content: space-around;
  padding: 20px 0px;
  border: solid 1px black;
  background: black;
}
.player-container {
  display: flex;
  align-items: center;
}
.player {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin: 0px 10px;
}
.player-name {
  margin: 5px 10px;
  color: white;
}
.player:nth-child(1) {
  background-color: blue;
}
.player:nth-child(2) {
  background-color: red;
}
.player-square {
  height: 10px;
  width: 10px;
  background-color: white;
  margin-right: 10px;
}
.player-circle {
  height: 10px;
  width: 10px;
  background-color: white;
  border-radius: 50%;
  margin-right: 10px;
}

.track-icons-container {
  display: flex;
  justify-content: center;
}

.track-icons {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  padding: 20px 0px;
  max-width: 80vw;
}

main {
  height: 100vh;
  width: 100vw;
  background-color: #e5e5f7;
  opacity: 0.8;
  background-image: repeating-linear-gradient(
      45deg,
      #707070 25%,
      transparent 25%,
      transparent 75%,
      #707070 75%,
      #707070
    ),
    repeating-linear-gradient(45deg, #707070 25%, #e5e5f7 25%, #e5e5f7 75%, #707070 75%, #707070);
  background-position:
    0 0,
    240px 240px;
  background-size: 480px 480px;
}
</style>
