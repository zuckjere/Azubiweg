<template>
    <section
      ref="sectionRef"
      class="py-24 bg-[#f0f1f2] overflow-hidden"
    >
      <div class="max-w-7xl mx-auto px-6">
  
        <!-- HEADER -->
        <div
          ref="headerRef"
          class="text-center max-w-3xl mx-auto mb-16"
        >
          <span
            class="inline-flex items-center px-4 py-2 rounded-full bg-[#3f56a2]/10 text-[#3f56a2] text-sm font-medium"
          >
            Nos Services
          </span>
  
          <h2 class="mt-6 text-4xl md:text-5xl font-bold text-gray-900">
            Nos services en bref
          </h2>
  
          <p class="mt-5 text-lg text-gray-600 leading-relaxed">
            Nous vous accompagnons à chaque étape de votre projet professionnel
            en Allemagne.
          </p>
        </div>
  
        <!-- CARDS -->
        <div
          ref="cardsContainer"
          class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8"
        >
  
          <!-- CARD 1 -->
          <div class="service-card bg-white rounded-3xl p-8 shadow-sm">
            <div
              class="w-16 h-16 rounded-2xl bg-[#3f56a2]/10 flex items-center justify-center mb-6"
            >
              <Icon
                icon="mdi:briefcase"
                width="34"
                class="text-[#3f56a2]"
              />
            </div>
  
            <h3 class="text-xl font-semibold text-gray-900">
              Placement professionnel
            </h3>
  
            <p class="mt-4 text-gray-600 leading-relaxed">
              Nous trouvons l'employeur qui correspond à vos qualifications,
              votre expérience et vos objectifs professionnels.
            </p>
          </div>
  
          <!-- CARD 2 -->
          <div class="service-card bg-white rounded-3xl p-8 shadow-sm">
            <div
              class="w-16 h-16 rounded-2xl bg-[#3f56a2]/10 flex items-center justify-center mb-6"
            >
              <Icon
                icon="mdi:file-document"
                width="34"
                class="text-[#3f56a2]"
              />
            </div>
  
            <h3 class="text-xl font-semibold text-gray-900">
              Reconnaissance des qualifications
            </h3>
  
            <p class="mt-4 text-gray-600 leading-relaxed">
              Assistance pour l'organisation, la préparation et la soumission
              de tous les documents nécessaires.
            </p>
          </div>
  
          <!-- CARD 3 -->
          <div class="service-card bg-white rounded-3xl p-8 shadow-sm">
            <div
              class="w-16 h-16 rounded-2xl bg-[#3f56a2]/10 flex items-center justify-center mb-6"
            >
              <Icon
                icon="mdi:home"
                width="34"
                class="text-[#3f56a2]"
              />
            </div>
  
            <h3 class="text-xl font-semibold text-gray-900">
              Relocalisation et intégration
            </h3>
  
            <p class="mt-4 text-gray-600 leading-relaxed">
              Aide à la recherche de logement, aux démarches administratives
              et à votre intégration en Allemagne.
            </p>
          </div>
  
        </div>
  
      </div>
    </section>
  </template>
  
  <script setup>
  import { ref, onMounted } from "vue";
  import { Icon } from "@iconify/vue";
  
  import gsap from "gsap";
  import { ScrollTrigger } from "gsap/ScrollTrigger";
  
  gsap.registerPlugin(ScrollTrigger);
  
  const sectionRef = ref(null);
  const headerRef = ref(null);
  const cardsContainer = ref(null);
  
  onMounted(() => {
  
    // Animation du header
    gsap.fromTo(
      headerRef.value,
      {
        opacity: 0,
        y: 60,
      },
      {
        opacity: 1,
        y: 0,
        duration: 1.2,
        ease: "power3.out",
        scrollTrigger: {
          trigger: sectionRef.value,
          start: "top 75%",
        },
      }
    );
  
    // Animation des cards
    const cards = cardsContainer.value.querySelectorAll(".service-card");
  
    gsap.fromTo(
      cards,
      {
        opacity: 0,
        y: 80,
        scale: 0.95,
      },
      {
        opacity: 1,
        y: 0,
        scale: 1,
        duration: 1.2,
        stagger: 0.25,
        ease: "power3.out",
        scrollTrigger: {
          trigger: cardsContainer.value,
          start: "top 80%",
        },
      }
    );
  
  });
  </script>
  
  <style scoped>
  .service-card {
    transition:
      transform 0.4s ease,
      box-shadow 0.4s ease;
  }
  
  .service-card:hover {
    transform: translateY(-10px);
    box-shadow:
      0 20px 40px rgba(0, 0, 0, 0.08);
  }
  </style>