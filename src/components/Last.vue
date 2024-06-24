<template>
  <section class="w-full mb-12">
    <wave class="w-full"></wave>
    <section class="container-section mx-auto px-4">
      <HeaderSection title="Turut Mengundang"></HeaderSection>
      <Card>
        <template v-slot:body>
          <div class="p-6 text-center">
            <p class="text-sm font-bold mb-4">Keluarga Besar Pria</p>
            <p class="text-sm mb-6">
              Keluarga Besar Bago<br>
              Keluarga Besar Us Olin - Taneo<br>
              Keluarga Besar SMP SATAP N Sunbaki<br>
            </p>
            <p class="text-sm font-bold mb-4">Keluarga Besar Wanita</p>
            <p class="text-sm mb-6">
              Keluarga Besar Kefi - Naif<br>
              Keluarga Besar Witin - Kleden<br>
              Keluarga Besar SMPN Satap Oetulu<br>
            </p>
            <p class="text-sm font-bold mb-4">Bapak & Mama Saksi</p>
            <p class="text-sm">
              Bapak Aryanto Th Santar, S.H - Ibu Adriana M G Abi, S.IP<br>
            </p>
          </div>
        </template>
        <template v-slot:footer>
          <div class="relative w-full">
            <img src="@/assets/images/couples.png" class="w-full" alt="Couples Image">
            <transition name="fade-in">
              <div class="absolute inset-0 flex flex-col items-center justify-center p-6 text-center bg-black bg-opacity-50">
                <p class="text-sm text-white mb-2">
                  We would like to thank you for sharing in our wedding celebration. We are grateful for your presence, warm wishes, and your generous gift. We look forward to our future together and to make more memories with you.
                </p>
                <p class="text-sm text-white mt-2 font-mono" style="font-style: italic;">Yang Berbahagia</p>
                <p class="text-sm text-white" style="font-family: 'Great Vibes', cursive; font-size: 25px; margin-top: 10px;">Rio & Rosi</p>
              </div>
            </transition>
          </div>
        </template>
      </Card>
    </section>
  </section>
</template>

<script setup>
import HeaderSection from '@/components/HeaderSection.vue'
import Card from '@/components/Card.vue'
import wave from '@/assets/svg/wave.svg'
</script>

<style>
.fade-in-enter-active {
  transition: opacity 0.5s ease;
}
.fade-in-enter {
  opacity: 0;
}
.fade-in-leave-to {
  opacity: 0;
}
</style>

