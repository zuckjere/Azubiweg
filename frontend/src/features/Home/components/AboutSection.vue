<template>
    <section ref="section" class="py-24 bg-white overflow-hidden">
  
      <div class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
  
        <!-- LEFT TEXT -->
        <div ref="textBlock" class="opacity-0 translate-y-12">
  
          <h2 class="text-3xl md:text-5xl font-bold text-gray-900 leading-tight">
            Bienvenue sur GermanJobConnect
          </h2>
  
          <p class="mt-6 text-gray-600 text-base md:text-lg leading-relaxed">
            Nous sommes experts dans le placement de travailleurs qualifiés étrangers en Allemagne.
            Notre objectif est de vous accompagner dans votre parcours professionnel grâce à un
            accompagnement personnalisé et des conseils avisés.
            Grâce à notre réseau d'employeurs de confiance, nous vous ouvrons les portes du marché de l'emploi allemand.
          </p>
  
          <button
            class="mt-8 bg-[#3f56a2] text-white px-6 py-3 rounded-full hover:scale-105 transition"
          >
            En savoir plus
          </button>
  
        </div>
  
        <!-- RIGHT IMAGE (BIG CARD) -->
        <div ref="imageBlock" class="relative flex justify-center opacity-0 translate-y-12">
  
          <div class="relative w-[420px] h-[520px] rounded-3xl overflow-hidden shadow-2xl">
  
            <img
              :src="currentImage"
              class="absolute inset-0 w-full h-full object-cover"
              :key="currentImage"
            />
  
            <!-- overlay soft -->
            <div class="absolute inset-0 bg-black/10"></div>
  
          </div>
  
        </div>
  
      </div>
  
    </section>
  </template>
  
  <script setup>
  import { ref, onMounted } from "vue"
  import gsap from "gsap"
  import { ScrollTrigger } from "gsap/ScrollTrigger"
  
  gsap.registerPlugin(ScrollTrigger)
  
  // images
  import img1 from "@/assets/img/docta.jpg"
  import img2 from "@/assets/img/ing.jpg"
  import img3 from "@/assets/img/inf.jpg"
  
  const images = [img1, img2, img3]
  const currentImage = ref(images[0])
  
  const section = ref(null)
  const textBlock = ref(null)
  const imageBlock = ref(null)
  
  let index = 0
  
  function changeImageSmooth() {
    index = (index + 1) % images.length
  
    gsap.to(imageBlock.value, {
      opacity: 0,
      scale: 0.98,
      duration: 0.6,
      ease: "power2.out",
      onComplete: () => {
        currentImage.value = images[index]
  
        gsap.to(imageBlock.value, {
          opacity: 1,
          scale: 1,
          duration: 0.8,
          ease: "power2.out"
        })
      }
    })
  }
  
  onMounted(() => {
  
    // 🔥 SCROLL ANIMATION (TEXT + IMAGE)
    gsap.to(textBlock.value, {
      opacity: 1,
      y: 0,
      duration: 1,
      ease: "power3.out",
      scrollTrigger: {
        trigger: section.value,
        start: "top 80%"
      }
    })
  
    gsap.to(imageBlock.value, {
      opacity: 1,
      y: 0,
      duration: 1,
      ease: "power3.out",
      scrollTrigger: {
        trigger: section.value,
        start: "top 80%"
      }
    })
  
    // 🔥 AUTO IMAGE CHANGE SMOOTH (3s)
    setInterval(() => {
      changeImageSmooth()
    }, 3000)
  })
  </script>