```vue
<template>
  <section
    ref="sectionRef"
    class="relative overflow-hidden bg-[#f0f1f2] py-20 sm:py-24 lg:py-28"
  >
    <!-- Background decoration -->
    <div
      class="
        pointer-events-none
        absolute
        -right-40
        top-20
        h-96
        w-96
        rounded-full
        bg-[#3f56a2]/5
        blur-3xl
      "
    ></div>

    <div
      class="
        pointer-events-none
        absolute
        -left-40
        bottom-0
        h-96
        w-96
        rounded-full
        bg-[#3f56a2]/5
        blur-3xl
      "
    ></div>

    <div class="relative mx-auto max-w-7xl px-6 lg:px-8">

      <!-- HEADER -->
      <div
        ref="headerRef"
        class="mx-auto mb-14 max-w-3xl text-center lg:mb-16"
      >

        <!-- Badge -->
        <span
          class="
            inline-flex
            items-center
            gap-2
            rounded-full
            border
            border-[#3f56a2]/10
            bg-[#3f56a2]/10
            px-4
            py-2
            text-sm
            font-semibold
            text-[#3f56a2]
          "
        >
          <span
            class="h-1.5 w-1.5 rounded-full bg-[#3f56a2]"
          ></span>

          Nos services
        </span>

        <!-- Title -->
        <h2
          class="
            mt-6
            text-[36px]
            font-bold
            leading-[1.15]
            tracking-tight
            text-gray-950
            sm:text-[40px]
            lg:text-[44px]
          "
        >
          Un accompagnement
          <span class="text-[#3f56a2]">
            de A à Z
          </span>
        </h2>

        <!-- Description -->
        <p
          class="
            mx-auto
            mt-5
            max-w-2xl
            text-[16px]
            leading-7
            text-gray-600
            sm:text-[17px]
            lg:text-[18px]
          "
        >
          Nous vous accompagnons à chaque étape de votre projet professionnel
          en Allemagne, de la recherche d'emploi jusqu'à votre intégration.
        </p>

      </div>

      <!-- CARDS -->
      <div
        ref="cardsContainer"
        class="
          grid
          grid-cols-1
          gap-7
          md:grid-cols-2
          lg:grid-cols-3
          lg:gap-8
        "
      >

        <!-- CARD 1 -->
        <article
          class="
            service-card
            group
            relative
            overflow-hidden
            rounded-3xl
            border
            border-gray-200/80
            bg-white
            p-8
            shadow-[0_10px_40px_rgba(0,0,0,0.04)]
            sm:p-9
          "
        >

          <!-- Top accent -->
          <div
            class="
              absolute
              left-0
              top-0
              h-1
              w-0
              bg-[#3f56a2]
              transition-all
              duration-500
              group-hover:w-full
            "
          ></div>

          <!-- Icon -->
          <div
            class="
              mb-7
              flex
              h-16
              w-16
              items-center
              justify-center
              rounded-2xl
              bg-[#3f56a2]/10
              text-[#3f56a2]
              transition-all
              duration-500
              group-hover:bg-[#3f56a2]
              group-hover:text-white
              group-hover:shadow-lg
              group-hover:shadow-[#3f56a2]/20
            "
          >
            <Icon
              icon="mdi:briefcase-outline"
              width="32"
              height="32"
            />
          </div>

          <!-- Title -->
          <h3
            class="
              text-[22px]
              font-bold
              leading-snug
              tracking-tight
              text-gray-900
            "
          >
            Placement professionnel
          </h3>

          <!-- Description -->
          <p
            class="
              mt-4
              text-[16px]
              leading-7
              text-gray-600
            "
          >
            Nous trouvons l'employeur qui correspond à vos qualifications,
            votre expérience et vos objectifs professionnels.
          </p>

          <!-- Link -->
          <div
            class="
              mt-7
              flex
              items-center
              gap-2
              text-[15px]
              font-semibold
              text-[#3f56a2]
            "
          >
            En savoir plus

            <Icon
              icon="mdi:arrow-right"
              width="18"
              height="18"
              class="
                transition-transform
                duration-300
                group-hover:translate-x-1
              "
            />
          </div>

        </article>

        <!-- CARD 2 -->
        <article
          class="
            service-card
            group
            relative
            overflow-hidden
            rounded-3xl
            border
            border-gray-200/80
            bg-white
            p-8
            shadow-[0_10px_40px_rgba(0,0,0,0.04)]
            sm:p-9
          "
        >

          <!-- Top accent -->
          <div
            class="
              absolute
              left-0
              top-0
              h-1
              w-0
              bg-[#3f56a2]
              transition-all
              duration-500
              group-hover:w-full
            "
          ></div>

          <!-- Icon -->
          <div
            class="
              mb-7
              flex
              h-16
              w-16
              items-center
              justify-center
              rounded-2xl
              bg-[#3f56a2]/10
              text-[#3f56a2]
              transition-all
              duration-500
              group-hover:bg-[#3f56a2]
              group-hover:text-white
              group-hover:shadow-lg
              group-hover:shadow-[#3f56a2]/20
            "
          >
            <Icon
              icon="mdi:file-document-check-outline"
              width="32"
              height="32"
            />
          </div>

          <!-- Title -->
          <h3
            class="
              text-[22px]
              font-bold
              leading-snug
              tracking-tight
              text-gray-900
            "
          >
            Reconnaissance des qualifications
          </h3>

          <!-- Description -->
          <p
            class="
              mt-4
              text-[16px]
              leading-7
              text-gray-600
            "
          >
            Assistance pour l'organisation, la préparation et la soumission
            de tous les documents nécessaires à la reconnaissance de vos
            qualifications.
          </p>

          <!-- Link -->
          <div
            class="
              mt-7
              flex
              items-center
              gap-2
              text-[15px]
              font-semibold
              text-[#3f56a2]
            "
          >
            En savoir plus

            <Icon
              icon="mdi:arrow-right"
              width="18"
              height="18"
              class="
                transition-transform
                duration-300
                group-hover:translate-x-1
              "
            />
          </div>

        </article>

        <!-- CARD 3 -->
        <article
          class="
            service-card
            group
            relative
            overflow-hidden
            rounded-3xl
            border
            border-gray-200/80
            bg-white
            p-8
            shadow-[0_10px_40px_rgba(0,0,0,0.04)]
            sm:p-9
            md:col-span-2
            lg:col-span-1
          "
        >

          <!-- Top accent -->
          <div
            class="
              absolute
              left-0
              top-0
              h-1
              w-0
              bg-[#3f56a2]
              transition-all
              duration-500
              group-hover:w-full
            "
          ></div>

          <!-- Icon -->
          <div
            class="
              mb-7
              flex
              h-16
              w-16
              items-center
              justify-center
              rounded-2xl
              bg-[#3f56a2]/10
              text-[#3f56a2]
              transition-all
              duration-500
              group-hover:bg-[#3f56a2]
              group-hover:text-white
              group-hover:shadow-lg
              group-hover:shadow-[#3f56a2]/20
            "
          >
            <Icon
              icon="mdi:home-city-outline"
              width="32"
              height="32"
            />
          </div>

          <!-- Title -->
          <h3
            class="
              text-[22px]
              font-bold
              leading-snug
              tracking-tight
              text-gray-900
            "
          >
            Relocalisation et intégration
          </h3>

          <!-- Description -->
          <p
            class="
              mt-4
              text-[16px]
              leading-7
              text-gray-600
            "
          >
            Aide à la recherche de logement, aux démarches administratives
            et à votre intégration professionnelle et personnelle en
            Allemagne.
          </p>

          <!-- Link -->
          <div
            class="
              mt-7
              flex
              items-center
              gap-2
              text-[15px]
              font-semibold
              text-[#3f56a2]
            "
          >
            En savoir plus

            <Icon
              icon="mdi:arrow-right"
              width="18"
              height="18"
              class="
                transition-transform
                duration-300
                group-hover:translate-x-1
              "
            />
          </div>

        </article>

      </div>

      <!-- BOTTOM MESSAGE -->
      <div
        ref="bottomRef"
        class="
          mx-auto
          mt-12
          flex
          max-w-2xl
          items-center
          justify-center
          gap-3
          text-center
        "
      >
        <Icon
          icon="mdi:check-circle-outline"
          width="22"
          height="22"
          class="shrink-0 text-[#3f56a2]"
        />

        <p
          class="
            text-[15px]
            leading-6
            text-gray-500
            sm:text-base
          "
        >
          Un accompagnement personnalisé pour construire votre avenir
          professionnel en Allemagne.
        </p>
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";
import { Icon } from "@iconify/vue";

import gsap from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const sectionRef = ref(null);
const headerRef = ref(null);
const cardsContainer = ref(null);
const bottomRef = ref(null);

let ctx = null;

onMounted(() => {
  ctx = gsap.context(() => {

    /* HEADER */
    gsap.fromTo(
      headerRef.value,
      {
        opacity: 0,
        y: 45,
      },
      {
        opacity: 1,
        y: 0,
        duration: 0.9,
        ease: "power3.out",
        scrollTrigger: {
          trigger: sectionRef.value,
          start: "top 80%",
          once: true,
        },
      }
    );

    /* CARDS */
    const cards =
      cardsContainer.value?.querySelectorAll(".service-card");

    if (cards?.length) {
      gsap.fromTo(
        cards,
        {
          opacity: 0,
          y: 55,
        },
        {
          opacity: 1,
          y: 0,
          duration: 0.85,
          stagger: 0.15,
          ease: "power3.out",
          scrollTrigger: {
            trigger: cardsContainer.value,
            start: "top 82%",
            once: true,
          },
        }
      );
    }

    /* BOTTOM MESSAGE */
    gsap.fromTo(
      bottomRef.value,
      {
        opacity: 0,
        y: 20,
      },
      {
        opacity: 1,
        y: 0,
        duration: 0.7,
        ease: "power2.out",
        scrollTrigger: {
          trigger: bottomRef.value,
          start: "top 92%",
          once: true,
        },
      }
    );

  }, sectionRef.value);
});

onBeforeUnmount(() => {
  ctx?.revert();
});
</script>

<style scoped>
.service-card {
  transform: translateZ(0);

  transition:
    transform 0.4s cubic-bezier(0.22, 1, 0.36, 1),
    box-shadow 0.4s cubic-bezier(0.22, 1, 0.36, 1),
    border-color 0.4s ease;
}

.service-card:hover {
  transform: translateY(-8px);

  border-color: rgba(63, 86, 162, 0.16);

  box-shadow:
    0 24px 50px rgba(0, 0, 0, 0.08);
}

@media (prefers-reduced-motion: reduce) {
  .service-card {
    transition: none;
  }

  .service-card:hover {
    transform: none;
  }
}
</style>
```
