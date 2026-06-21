<template>
    <section
      ref="sectionRef"
      class="relative py-32 overflow-hidden"
    >
      <!-- BACKGROUND IMAGE -->
      <img
        :src="partImage"
        alt="German Job Connect"
        class="absolute inset-0 w-full h-full object-cover scale-110"
      />
  
      <!-- BLUE OVERLAY -->
      <div
        class="absolute inset-0 bg-[#2f4e9c]/85 backdrop-blur-[3px]"
      ></div>
  
      <!-- CONTENT -->
      <div
        class="relative z-10 max-w-5xl mx-auto px-6 text-center"
      >
        <div ref="contentRef">
  
          <span
            class="inline-flex items-center px-4 py-2 rounded-full bg-white/10 text-white border border-white/20"
          >
            Votre avenir commence ici
          </span>
  
          <h2
            class="mt-8 text-4xl md:text-6xl font-bold text-white leading-tight"
          >
            Prêt pour la prochaine étape ?
          </h2>
  
          <p
            class="mt-6 text-lg md:text-xl text-white/90 leading-relaxed max-w-3xl mx-auto"
          >
            Démarrons ensemble votre carrière en Allemagne.
            Contactez-nous dès aujourd'hui ou postulez directement en ligne.
          </p>
  
          <div
            ref="buttonsRef"
            class="mt-12 flex flex-col sm:flex-row justify-center gap-5"
          >
            <button
              class="bg-white text-[#3c549e] px-8 py-4 rounded-full font-semibold hover:scale-105 transition-all duration-300 shadow-xl"
            >
              Postulez maintenant
            </button>
  
            <button
              class="border border-white text-white px-8 py-4 rounded-full font-semibold hover:bg-white hover:text-[#3c549e] transition-all duration-300"
            >
              Nous contacter
            </button>
          </div>
  
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import { ref, onMounted } from "vue";
  import gsap from "gsap";
  import { ScrollTrigger } from "gsap/ScrollTrigger";
  
  import partImage from "@/assets/img/part.jpg";
  
  gsap.registerPlugin(ScrollTrigger);
  
  const sectionRef = ref(null);
  const contentRef = ref(null);
  const buttonsRef = ref(null);
  
  onMounted(() => {
  
    const tl = gsap.timeline({
      scrollTrigger: {
        trigger: sectionRef.value,
        start: "top 75%",
        toggleActions: "play none none none",
      },
    });
  
    tl.fromTo(
      contentRef.value,
      {
        opacity: 0,
        y: 80,
      },
      {
        opacity: 1,
        y: 0,
        duration: 1.4,
        ease: "power4.out",
      }
    );
  
    tl.fromTo(
      buttonsRef.value.children,
      {
        opacity: 0,
        y: 30,
        scale: 0.95,
      },
      {
        opacity: 1,
        y: 0,
        scale: 1,
        stagger: 0.15,
        duration: 0.9,
        ease: "power3.out",
      },
      "-=0.6"
    );
  
    // léger effet parallax
    gsap.to(sectionRef.value.querySelector("img"), {
      yPercent: 15,
      ease: "none",
      scrollTrigger: {
        trigger: sectionRef.value,
        start: "top bottom",
        end: "bottom top",
        scrub: true,
      },
    });
  
  });
  </script>
  
  <style scoped>
  section {
    min-height: 70vh;
  }
  </style>