<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'
import { Icon } from '@iconify/vue'
import { RouterLink } from 'vue-router'
import logo from '@/assets/img/send.jpg'

const isScrolled = ref(false)
const isOpen = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 80
}

const toggleMenu = () => {
  isOpen.value = !isOpen.value
}

const closeMenu = () => {
  isOpen.value = false
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <header
    :class="[
      'fixed top-0 left-0 w-full z-50 transition-all duration-500',
      isScrolled
        ? 'bg-[#2864e9] shadow-lg backdrop-blur-md'
        : 'bg-transparent'
    ]"
  >
    <div class="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between">

      <!-- LOGO -->
      <RouterLink
        to="/"
        class="flex items-center gap-3 hover:scale-[1.03] transition-all duration-300"
      >
        <img
          :src="logo"
          alt="Azubiweg logo"
          class="w-9 h-9 rounded-md object-cover shadow-md"
        />

        <span class="text-white font-bold text-xl tracking-wide">
          Azubiweg
        </span>
      </RouterLink>

      <!-- DESKTOP MENU -->
      <nav class="hidden md:flex items-center gap-10 text-white text-sm font-medium">

        <RouterLink to="/" class="nav-link">Home</RouterLink>
        <RouterLink to="/services" class="nav-link">Services</RouterLink>
        <RouterLink to="/candidats" class="nav-link">Candidats</RouterLink>
        <RouterLink to="/success-stories" class="nav-link">
          Histoires à succès
        </RouterLink>
        <RouterLink to="/about" class="nav-link">À propos</RouterLink>
        <RouterLink to="/contact" class="nav-link">Contact</RouterLink>

      </nav>

      <!-- CTA DESKTOP -->
      <div class="hidden md:flex items-center gap-3">

        <a
          href="tel:+243970213159"
          class="flex items-center gap-2 bg-white/10 hover:bg-white/25 hover:scale-[1.03] transition-all duration-300 px-4 py-1.5 rounded-full text-sm text-white"
        >
          <Icon icon="mdi:phone" width="18" />
          Appel
        </a>

        <a
          href="https://wa.me/243970213159"
          target="_blank"
          class="flex items-center gap-2 bg-green-500 hover:bg-green-600 hover:scale-[1.03] transition-all duration-300 px-4 py-1.5 rounded-full text-sm text-white"
        >
          <Icon icon="mdi:whatsapp" width="18" />
          WhatsApp
        </a>

      </div>

      <!-- HAMBURGER -->
      <button
        class="md:hidden relative w-10 h-10 flex flex-col justify-center items-center"
        @click="toggleMenu"
      >
        <span
          class="block w-6 h-0.5 bg-white transition-all duration-500"
          :class="isOpen ? 'rotate-45 translate-y-1.5' : '-translate-y-1.5'"
        />
        <span
          class="block w-6 h-0.5 bg-white transition-all duration-500"
          :class="isOpen ? 'opacity-0' : 'opacity-100'"
        />
        <span
          class="block w-6 h-0.5 bg-white transition-all duration-500"
          :class="isOpen ? '-rotate-45 -translate-y-1.5' : 'translate-y-1.5'"
        />
      </button>

    </div>

    <!-- MOBILE MENU -->
    <div
      class="md:hidden overflow-hidden bg-[#1f3f8a] transition-all duration-700 ease-in-out"
      :class="isOpen ? 'max-h-[500px] py-6 opacity-100' : 'max-h-0 py-0 opacity-0'"
    >
      <div class="flex flex-col px-6 space-y-5 text-white text-sm">

        <RouterLink to="/" class="mobile-link" @click="closeMenu">Home</RouterLink>
        <RouterLink to="/services" class="mobile-link" @click="closeMenu">Services</RouterLink>
        <RouterLink to="/candidats" class="mobile-link" @click="closeMenu">Candidats</RouterLink>
        <RouterLink to="/success-stories" class="mobile-link" @click="closeMenu">Histoires</RouterLink>
        <RouterLink to="/about" class="mobile-link" @click="closeMenu">À propos</RouterLink>
        <RouterLink to="/contact" class="mobile-link" @click="closeMenu">Contact</RouterLink>

        <a
          href="tel:+243970213159"
          class="flex items-center justify-center gap-2 bg-white/10 hover:bg-white/20 transition py-2 rounded-full mt-3"
          @click="closeMenu"
        >
          <Icon icon="mdi:phone" width="18" />
          Appel
        </a>

        <a
          href="https://wa.me/243970213159"
          target="_blank"
          class="flex items-center justify-center gap-2 bg-green-500 hover:bg-green-600 transition py-2 rounded-full"
          @click="closeMenu"
        >
          <Icon icon="mdi:whatsapp" width="18" />
          WhatsApp
        </a>

      </div>
    </div>
  </header>
</template>

<style scoped>
.nav-link {
  opacity: 0.8;
  position: relative;
  transition: all 0.3s ease;
}

.nav-link:hover {
  opacity: 1;
}

.nav-link::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: -4px;
  height: 2px;
  width: 0%;
  background: white;
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}

.mobile-link {
  opacity: 0.85;
  transition: 0.3s;
}

.mobile-link:hover {
  opacity: 1;
  transform: translateX(4px);
}
</style>