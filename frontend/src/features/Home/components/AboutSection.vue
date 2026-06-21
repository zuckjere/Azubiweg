<template>
    <section
      ref="section"
      class="py-24 bg-[#f0f1f2] overflow-hidden"
    >
      <div
        class="max-w-7xl mx-auto px-6 grid grid-cols-1 lg:grid-cols-2 gap-20 items-center"
      >
  
        <!-- LEFT CONTENT -->
        <div
          ref="textBlock"
          class="opacity-0"
        >
          <span
            class="inline-flex items-center px-4 py-2 rounded-full bg-[#3f56a2]/10 text-[#3f56a2] font-medium"
          >
            À propos de nous
          </span>
  
          <h2
            class="mt-6 text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight"
          >
            Bienvenue sur
            <span class="text-[#3f56a2]">
              Azubiweg
            </span>
          </h2>
  
          <p
            class="mt-8 text-gray-600 text-lg leading-relaxed max-w-xl"
          >
            Nous sommes experts dans le placement de travailleurs qualifiés
            étrangers en Allemagne. Notre objectif est de vous accompagner
            dans votre parcours professionnel grâce à un accompagnement
            personnalisé et des conseils avisés.
          </p>
  
          <p
            class="mt-4 text-gray-600 text-lg leading-relaxed max-w-xl"
          >
            Grâce à notre réseau d'employeurs de confiance, nous vous ouvrons
            les portes du marché de l'emploi allemand et facilitons votre
            intégration professionnelle.
          </p>
  
          <button
            class="mt-10 bg-[#3f56a2] text-white px-8 py-4 rounded-full font-medium hover:scale-105 transition-all duration-300 shadow-lg"
          >
            En savoir plus
          </button>
        </div>
  
        <!-- RIGHT IMAGE -->
        <div
          ref="imageBlock"
          class="relative flex justify-center opacity-0"
        >
          <div
            class="relative w-full max-w-[620px] h-[650px] rounded-[32px] overflow-hidden shadow-[0_30px_80px_rgba(0,0,0,0.15)]"
          >
  
            <img
              :src="currentImage"
              :key="currentImage"
              class="absolute inset-0 w-full h-full object-cover"
              alt="German Job Connect"
            />
  
            <!-- Overlay -->
            <div
              class="absolute inset-0 bg-gradient-to-t from-black/30 via-transparent to-transparent"
            />
  
          </div>
        </div>
  
      </div>
    </section>
  </template>
  
  <script setup>
  import { ref, onMounted, onUnmounted } from "vue";
  import gsap from "gsap";
  import { ScrollTrigger } from "gsap/ScrollTrigger";
  
  import img1 from "@/assets/img/docta.jpg";
  import img2 from "@/assets/img/ing.jpg";
  import img3 from "@/assets/img/inf.jpg";
  
  gsap.registerPlugin(ScrollTrigger);
  
  const images = [img1, img2, img3];
  
  const currentImage = ref(images[0]);
  
  const section = ref(null);
  const textBlock = ref(null);
  const imageBlock = ref(null);
  
  let index = 0;
  let interval = null;
  
  function changeImageSmooth() {
    index = (index + 1) % images.length;
  
    gsap.to(imageBlock.value, {
      opacity: 0.4,
      scale: 1.03,
      duration: 1,
      ease: "power2.inOut",
      onComplete: () => {
        currentImage.value = images[index];
  
        gsap.fromTo(
          imageBlock.value,
          {
            opacity: 0.4,
            scale: 1.03,
          },
          {
            opacity: 1,
            scale: 1,
            duration: 1.4,
            ease: "power3.out",
          }
        );
      },
    });
  }
  
  onMounted(() => {
  
    const tl = gsap.timeline({
      scrollTrigger: {
        trigger: section.value,
        start: "top 75%",
        toggleActions: "play none none none",
      },
    });
  
    tl.fromTo(
      textBlock.value,
      {
        opacity: 0,
        x: -80,
        y: 30,
      },
      {
        opacity: 1,
        x: 0,
        y: 0,
        duration: 1.4,
        ease: "power4.out",
      }
    ).fromTo(
      imageBlock.value,
      {
        opacity: 0,
        x: 80,
        y: 30,
        scale: 0.92,
      },
      {
        opacity: 1,
        x: 0,
        y: 0,
        scale: 1,
        duration: 1.6,
        ease: "power4.out",
      },
      "-=1"
    );
  
    interval = setInterval(() => {
      changeImageSmooth();
    }, 4500);
  });
  
  onUnmounted(() => {
    if (interval) {
      clearInterval(interval);
    }
  });
  </script>