<template>
  <section class="w-full bg-gradient-to-b from-customGreen to-customBrown">
    <wave class="fill-white" />
    <section class="container-section">
      <HeaderSection text-color="text-gray-100" title="Mempelai Pria dan Wanita"
        subtitle="Ya Tuhan, dengan penuh kerendahan hati kami memohon kasih dan berkat-Mu, Izinkanlah kami menyatukan dua insan dari dua keluarga ini agar menjadi pasangan yang selalu mendapatkan rahmat-Mu. Semoga cinta mereka selalu dalam perlindungan-Mu dan dipenuhi dengan damai sejahtera serta sukacita. Amin." />
      <Profile></Profile>
    </section>
  </section>
</template>

<script setup>

import HeaderSection from '@/components/HeaderSection.vue'
import Profile from '@/components/Profile.vue'
import Timelines from '@/components/Timelines.vue'
import wave from '@/assets/svg/wave.svg'

</script>
