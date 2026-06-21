<script setup lang="ts">
import HeroSection from '@/features/Home/components/HeroSection.vue'
import AboutSection from '@/features/Home/components/AboutSection.vue'
import Service from '@/features/Home/components/Service.vue'
import Partenaire from '@/features/Home/components/Partenaire.vue'
</script>

<template>
  <div class="min-h-screen bg-white">

    <!-- HERO -->
    <main>
      <HeroSection />
      <AboutSection />
      <Service />
      <Partenaire />
    </main>

  </div>
</template>