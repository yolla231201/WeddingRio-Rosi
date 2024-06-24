<!-- <template>
  <section class="w-full bg-couples bg-cover h-screen">
    <section class="container-section h-screen grid content-end">
      <div
        class="animate__animated animate__fadeInUpBig text-gray-100 text-center bg-gray-800 bg-opacity-50 backdrop-blur-sm rounded-t-3xl px-6 py-10">
        <p>Pernikahan</p>
        <h1 class="tangerine-font text-title font-bold">{{ couples.join(' & ') }}</h1>
        <decoration class="fill-amber-400 mx-auto w-3/12 mb-3"></decoration>
        <p class="text-sm"></p>
        <p class="font-medium">Kepada Bapak/Ibu Yang Terhormat</p>
        <p class="font-medium my-2 text-lg">{{ query.to }}</p>
        <small>Izinkan kami turut mengundang anda dalam acara kami</small>
        

      </div>
    </section>
  </section>
</template>

<script setup>

import { computed } from 'vue'
import { useRoute } from 'vue-router'
import decoration from '@/assets/svg/icon.svg'

const couples = ['Rio', 'Rossy']

const route = useRoute()
let query = computed(() => route.query)

if (route.query.to === undefined) query = { to: 'Saudara/i' }

</script> -->


<template>
  <section class="w-full bg-couples bg-cover h-screen">
    <section class="container-section h-screen grid content-end">
      <div
        class="animate__animated animate__fadeInUpBig text-gray-100 text-center bg-customGreen bg-opacity-40 backdrop-blur-sm rounded-t-3xl px-6 py-10">
        <p style="font-style: italic; margin-bottom: -15px;">Save The Date</p>
        <p>___________________</p>
        <p style="font-family: Arial, Helvetica, sans-serif; font-weight: 800;">02 - 07 - 2024</p>
        <h1 class="tangerine-font text-title font-bold">{{ couples.join(' & ') }}</h1>
        <img class="mx-auto w-3/12 mb-3" :src="decoration" alt="Decoration"/>
        <p class="text-sm"></p>
        <p class="font-medium">Kepada Bapak/Ibu Yang Terhormat</p>
        <p class="font-medium my-2 text-lg">{{ toName }}</p>
        <small>Izinkan kami turut mengundang anda dalam acara kami</small>
      </div>
    </section>
  </section>
</template>


<script setup>
import { computed } from 'vue'
import { useRoute } from 'vue-router'
// Import gambar dekorasi
import decoration from '@/assets/images/icon2.png'

// Pasangan
const couples = ['Rio', 'Rossy']

// Mendapatkan rute saat ini
const route = useRoute()

// Properti komputasi untuk mendapatkan nama tamu dari query string
const toName = computed(() => {
  return route.query.to || 'Saudara/i'
})
</script>

<style scoped>
img {
  display: block;
  margin: 0 auto;
}
</style>

