<template>
  <section class="fixed bottom-24 pl-2">
    <button class="button" @click="control">
      <i v-if="!isPlayed" class="fa-solid fa-volume-off"></i>
      <i v-else class="fa-solid fa-volume-high"></i>
    </button>
    <!-- <button @click="giftAction" class="button">
      <i class="fa-solid fa-gift"></i>
    </button> -->
  </section>
  <audio ref="audioEl" loop>
    <source src="@/assets/audio/backsound.mp3" type="audio/mp3">
    Your browser does not support the audio element.
  </audio>
</template>

<script setup>
import { ref, watch, computed, onMounted } from 'vue'
import { useState } from '@/stores/state.js'

const state = useState()

const audioEl = ref(null)
const isPlayed = ref(false)  // Default to false, we'll start playing on user interaction

const isAudioPlay = computed(() => state.isAudioPlay)

const control = () => {
  isPlayed.value = !isPlayed.value
  if (isPlayed.value) {
    audioEl.value.play()
  } else {
    audioEl.value.pause()
  }
}

watch(isAudioPlay, (newVal) => {
  if (newVal) {
    audioEl.value.play()
  } else {
    audioEl.value.pause()
  }
})

const playAudioOnInteraction = () => {
  if (!isPlayed.value) {
    audioEl.value.play().then(() => {
      isPlayed.value = true
    }).catch((error) => {
      console.error('Playback failed:', error)
    })
  }
}

onMounted(() => {
  // Add event listeners to detect user interaction
  document.addEventListener('click', playAudioOnInteraction, { once: true })
  document.addEventListener('scroll', playAudioOnInteraction, { once: true })
  document.addEventListener('keypress', playAudioOnInteraction, { once: true })
})

const giftAction = () => {
  setTimeout(() => {
    document.querySelector('#envelope').scrollIntoView({ behavior: 'smooth' })
  }, 300)
}
</script>

<style scoped>
.button {
  @apply bg-gray-600 bg-opacity-50 backdrop-blur-sm border border-gray-800 rounded-full text-lg grid place-items-center text-amber-100 z-50 mb-2;
  height: 40px;
  width: 40px;
}

.button i {
  color: black;
}
</style>
