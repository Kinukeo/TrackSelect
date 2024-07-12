<script setup>
defineProps(['imageSrc', 'trackName'])
</script>

<template>
  <div class="track-block">
    <img class="track-image" style="height: 90px; width: 160px" :src="imageSrc" />
    <h1>{{ trackName }}</h1>
  </div>
</template>

<style scoped>
.track-block {
  display: flex;
  flex-direction: column;
  flex-basis: 20%;
  margin: 10px 10px;
  padding: 10px 10px;
  text-align: center;
  align-items: center;
  color: #ed6802;
  background: black;
}

.track-image {
  padding-top: 20px;
}
</style>
