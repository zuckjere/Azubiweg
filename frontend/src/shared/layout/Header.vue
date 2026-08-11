```vue
<script setup lang="ts">
import { ref, onMounted, onUnmounted, nextTick } from 'vue'
import { Icon } from '@iconify/vue'
import { RouterLink, useRouter } from 'vue-router'
import logo from '@/assets/img/send.jpg'

const router = useRouter()

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

/**
 * Navigation vers une section de la page d'accueil
 */
const goToSection = async (section: string) => {
  closeMenu()

  /*
   * Si nous sommes déjà sur la page d'accueil,
   * on cherche directement la section.
   */
  if (router.currentRoute.value.path === '/') {
    await nextTick()

    const element = document.getElementById(section)

    if (element) {
      element.scrollIntoView({
        behavior: 'smooth',
        block: 'start',
      })
    }

    return
  }

  /*
   * Si nous sommes sur une autre page,
   * on revient d'abord sur la Home avec l'ancre.
   */
  await router.push({
    path: '/',
    hash: `#${section}`,
  })

  await nextTick()

  setTimeout(() => {
    const element = document.getElementById(section)

    if (element) {
      element.scrollIntoView({
        behavior: 'smooth',
        block: 'start',
      })
    }
  }, 100)
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)

  /*
   * Si l'URL contient déjà une ancre,
   * par exemple /#services,
   * on descend automatiquement vers la section.
   */
  if (window.location.hash) {
    const section = window.location.hash.substring(1)

    setTimeout(() => {
      const element = document.getElementById(section)

      if (element) {
        element.scrollIntoView({
          behavior: 'smooth',
          block: 'start',
        })
      }
    }, 300)
  }
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <header
    :class="[
      'fixed left-0 top-0 z-50 w-full transition-all duration-500',
      isScrolled
        ? 'bg-[#2864e9] shadow-lg backdrop-blur-md'
        : 'bg-transparent',
    ]"
  >

    <!-- HEADER -->
    <div
      class="
        mx-auto
        flex
        max-w-7xl
        items-center
        justify-between
        px-6
        py-4
      "
    >

      <!-- LOGO -->
      <RouterLink
        to="/"
        class="
          flex
          items-center
          gap-3
          transition-all
          duration-300
          hover:scale-[1.03]
        "
        @click="closeMenu"
      >
        <img
          :src="logo"
          alt="Azubiweg logo"
          class="
            h-9
            w-9
            rounded-md
            object-cover
            shadow-md
          "
        />

        <span
          class="
            text-xl
            font-bold
            tracking-wide
            text-white
          "
        >
          Azubiweg
        </span>
      </RouterLink>


      <!-- DESKTOP NAVIGATION -->
      <nav
        class="
          hidden
          items-center
          gap-10
          text-sm
          font-medium
          text-white
          md:flex
        "
      >

        <!-- HOME -->
        <button
          type="button"
          class="nav-link"
          @click="goToSection('home')"
        >
          Home
        </button>


        <!-- SERVICES -->
        <button
          type="button"
          class="nav-link"
          @click="goToSection('services')"
        >
          Services
        </button>


        <!-- CANDIDATS -->
        <button
          type="button"
          class="nav-link"
          @click="goToSection('candidats')"
        >
          Candidats
        </button>


        <!-- HISTOIRES -->
        <button
          type="button"
          class="nav-link"
          @click="goToSection('success-stories')"
        >
          Histoires à succès
        </button>


        <!-- À PROPOS -->
        <button
          type="button"
          class="nav-link"
          @click="goToSection('about')"
        >
          À propos
        </button>


        <!-- CONTACT -->
        <button
          type="button"
          class="nav-link"
          @click="goToSection('contact')"
        >
          Contact
        </button>

      </nav>


      <!-- CTA -->
      <div
        class="
          hidden
          items-center
          gap-3
          md:flex
        "
      >

        <!-- PHONE -->
        <a
          href="tel:+243970213159"
          class="
            flex
            items-center
            gap-2
            rounded-full
            bg-white/10
            px-4
            py-1.5
            text-sm
            text-white
            transition-all
            duration-300
            hover:scale-[1.03]
            hover:bg-white/25
          "
        >
          <Icon
            icon="mdi:phone"
            width="18"
          />

          Appel
        </a>


        <!-- WHATSAPP -->
        <a
          href="https://wa.me/243970213159"
          target="_blank"
          rel="noopener noreferrer"
          class="
            flex
            items-center
            gap-2
            rounded-full
            bg-green-500
            px-4
            py-1.5
            text-sm
            text-white
            transition-all
            duration-300
            hover:scale-[1.03]
            hover:bg-green-600
          "
        >
          <Icon
            icon="mdi:whatsapp"
            width="18"
          />

          WhatsApp
        </a>

      </div>


      <!-- MOBILE HAMBURGER -->
      <button
        type="button"
        aria-label="Menu"
        :aria-expanded="isOpen"
        class="
          relative
          flex
          h-10
          w-10
          items-center
          justify-center
          md:hidden
        "
        @click="toggleMenu"
      >

        <span
          class="
            absolute
            h-0.5
            w-6
            bg-white
            transition-all
            duration-500
          "
          :class="
            isOpen
              ? 'rotate-45'
              : '-translate-y-2'
          "
        ></span>

        <span
          class="
            absolute
            h-0.5
            w-6
            bg-white
            transition-all
            duration-500
          "
          :class="
            isOpen
              ? 'opacity-0'
              : 'opacity-100'
          "
        ></span>

        <span
          class="
            absolute
            h-0.5
            w-6
            bg-white
            transition-all
            duration-500
          "
          :class="
            isOpen
              ? '-rotate-45'
              : 'translate-y-2'
          "
        ></span>

      </button>

    </div>


    <!-- MOBILE MENU -->
    <div
      class="
        overflow-hidden
        bg-[#1f3f8a]
        transition-all
        duration-500
        ease-in-out
        md:hidden
      "
      :class="
        isOpen
          ? 'max-h-[600px] py-6 opacity-100'
          : 'max-h-0 py-0 opacity-0'
      "
    >

      <div
        class="
          flex
          flex-col
          space-y-5
          px-6
          text-sm
          text-white
        "
      >

        <!-- HOME -->
        <button
          type="button"
          class="mobile-link"
          @click="goToSection('home')"
        >
          Home
        </button>


        <!-- SERVICES -->
        <button
          type="button"
          class="mobile-link"
          @click="goToSection('services')"
        >
          Services
        </button>


        <!-- CANDIDATS -->
        <button
          type="button"
          class="mobile-link"
          @click="goToSection('candidats')"
        >
          Candidats
        </button>


        <!-- HISTOIRES -->
        <button
          type="button"
          class="mobile-link"
          @click="goToSection('success-stories')"
        >
          Histoires à succès
        </button>


        <!-- À PROPOS -->
        <button
          type="button"
          class="mobile-link"
          @click="goToSection('about')"
        >
          À propos
        </button>


        <!-- CONTACT -->
        <button
          type="button"
          class="mobile-link"
          @click="goToSection('contact')"
        >
          Contact
        </button>


        <!-- PHONE -->
        <a
          href="tel:+243970213159"
          class="
            mt-3
            flex
            items-center
            justify-center
            gap-2
            rounded-full
            bg-white/10
            py-2.5
            transition
            hover:bg-white/20
          "
          @click="closeMenu"
        >
          <Icon
            icon="mdi:phone"
            width="18"
          />

          Appel
        </a>


        <!-- WHATSAPP -->
        <a
          href="https://wa.me/243970213159"
          target="_blank"
          rel="noopener noreferrer"
          class="
            flex
            items-center
            justify-center
            gap-2
            rounded-full
            bg-green-500
            py-2.5
            transition
            hover:bg-green-600
          "
          @click="closeMenu"
        >
          <Icon
            icon="mdi:whatsapp"
            width="18"
          />

          WhatsApp
        </a>

      </div>

    </div>

  </header>
</template>


<style scoped>
/* ================================
   DESKTOP LINKS
================================ */

.nav-link {
  position: relative;

  border: 0;

  background: transparent;

  padding: 0;

  cursor: pointer;

  color: white;

  font: inherit;

  opacity: 0.82;

  transition:
    opacity 0.3s ease,
    transform 0.3s ease;
}

.nav-link:hover {
  opacity: 1;

  transform: translateY(-1px);
}


/* Underline */

.nav-link::after {
  content: '';

  position: absolute;

  left: 0;
  bottom: -7px;

  width: 0;
  height: 2px;

  border-radius: 999px;

  background: white;

  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}


/* ================================
   MOBILE LINKS
================================ */

.mobile-link {
  width: 100%;

  border: 0;

  background: transparent;

  padding: 0;

  cursor: pointer;

  color: white;

  text-align: left;

  font: inherit;

  opacity: 0.85;

  transition:
    opacity 0.3s ease,
    transform 0.3s ease;
}

.mobile-link:hover {
  opacity: 1;

  transform: translateX(5px);
}


/* ================================
   FOCUS
================================ */

.nav-link:focus-visible,
.mobile-link:focus-visible {
  outline: 2px solid white;

  outline-offset: 5px;
}


/* ================================
   REDUCED MOTION
================================ */

@media (prefers-reduced-motion: reduce) {
  .nav-link,
  .nav-link::after,
  .mobile-link {
    transition: none;
  }
}
</style>
```
