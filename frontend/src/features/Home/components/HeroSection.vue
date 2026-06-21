<template>
    <section class="relative w-full h-[120vh] overflow-hidden">
  
      <!-- BACKGROUND -->
      <div class="absolute inset-0">
        <img
          src="@/assets/img/hero.jpg"
          alt="hero"
          class="w-full h-full object-cover scale-105 blur-sm"
        />
  
        <div
          class="absolute inset-0"
          style="
            background: linear-gradient(
              135deg,
              rgba(63, 86, 162, 0.9),
              rgba(63, 86, 162, 0.6)
            );
          "
        ></div>
      </div>
  
      <!-- CONTENT -->
      <div class="relative z-10 flex items-center justify-center h-full px-6">
  
        <div class="max-w-4xl text-center text-white">
  
          <!-- TITLE -->
          <h1
            ref="title"
            class="text-3xl sm:text-4xl md:text-6xl font-extrabold leading-tight tracking-tight opacity-0 translate-y-10"
          >
            Votre tremplin pour une carrière réussie en Allemagne et Autriche
          </h1>
  
          <!-- SUBTITLE -->
          <p
            ref="text"
            class="mt-6 text-base sm:text-lg md:text-xl text-white/90 leading-relaxed max-w-2xl mx-auto opacity-0 translate-y-10"
          >
            Nous accompagnons les professionnels de la santé, de l'informatique et de l'ingénierie
            dans leur projet de s'installer en Allemagne.
          </p>
  
          <!-- CTA -->
          <div
            ref="buttons"
            class="mt-10 flex flex-col sm:flex-row gap-5 justify-center items-center opacity-0 translate-y-10"
          >
  
            <!-- PRIMARY → CANDIDATS -->
            <RouterLink
              to="/candidats"
              class="flex items-center gap-2 bg-white text-[#3f56a2] px-8 py-3.5 rounded-full font-semibold text-sm sm:text-base shadow-lg hover:scale-105 transition"
            >
              <span>Postuler maintenant</span>
  
              <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" fill="none"
                viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                  d="M14 5l7 7m0 0l-7 7m7-7H3" />
              </svg>
            </RouterLink>
  
            <!-- SECONDARY → SERVICES -->
            <RouterLink
              to="/services"
              class="flex items-center gap-2 border border-white px-8 py-3.5 rounded-full text-sm sm:text-base font-medium hover:bg-white hover:text-[#3f56a2] transition"
            >
              <span>Apprendre encore plus</span>
  
              <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" fill="none"
                viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                  d="M9 5l7 7-7 7" />
              </svg>
            </RouterLink>
  
          </div>
  
        </div>
      </div>
  
    </section>
  </template>
  
  <script setup>
  import { onMounted, ref } from "vue";
  import gsap from "gsap";
  
  const title = ref(null);
  const text = ref(null);
  const buttons = ref(null);
  
  onMounted(() => {
    const tl = gsap.timeline({ defaults: { ease: "power3.out" } });
  
    tl.to(title.value, {
      opacity: 1,
      y: 0,
      duration: 0.9
    })
    .to(text.value, {
      opacity: 1,
      y: 0,
      duration: 0.8
    }, "-=0.5")
    .to(buttons.value, {
      opacity: 1,
      y: 0,
      duration: 0.8
    }, "-=0.4");
  });
  </script>