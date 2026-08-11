```vue
<template>
  <footer class="bg-[#111827] text-white">

    <!-- MAIN FOOTER -->
    <div class="mx-auto max-w-7xl px-6 py-16 lg:px-8 lg:py-20">

      <div class="grid gap-12 lg:grid-cols-[1.4fr_1fr_0.8fr]">

        <!-- BRAND -->
        <div class="max-w-md">
          <a
            href="#"
            class="inline-flex items-center gap-3"
          >
            <div
              class="
                flex
                h-11
                w-11
                items-center
                justify-center
                rounded-xl
                bg-[#2563EB]
                text-lg
                font-bold
              "
            >
              A
            </div>

            <span class="text-xl font-bold tracking-tight">
              Azubiweg
            </span>
          </a>

          <p
            class="
              mt-6
              max-w-sm
              text-sm
              leading-7
              text-gray-400
            "
          >
            Votre tremplin vers la réussite professionnelle en Allemagne.
            Nous vous accompagnons dans vos démarches et votre projet
            professionnel.
          </p>

          <!-- SOCIALS -->
          <div class="mt-7 flex items-center gap-3">

            <!-- Facebook -->
            <a
              href="#"
              aria-label="Facebook"
              class="
                flex
                h-10
                w-10
                items-center
                justify-center
                rounded-full
                border
                border-gray-700
                bg-gray-800/50
                text-gray-400
                transition
                hover:border-[#2563EB]
                hover:bg-[#2563EB]
                hover:text-white
              "
            >
              <svg
                viewBox="0 0 24 24"
                fill="currentColor"
                class="h-4 w-4"
              >
                <path
                  d="M13.5 22v-8h2.75l.4-3h-3.15V9.08c0-.87.24-1.46 1.5-1.46h1.76V4.94c-.3-.04-1.32-.13-2.5-.13-2.48 0-4.18 1.51-4.18 4.29V11H7.25v3h2.83v8h3.42Z"
                />
              </svg>
            </a>

            <!-- Instagram -->
            <a
              href="#"
              aria-label="Instagram"
              class="
                flex
                h-10
                w-10
                items-center
                justify-center
                rounded-full
                border
                border-gray-700
                bg-gray-800/50
                text-gray-400
                transition
                hover:border-[#2563EB]
                hover:bg-[#2563EB]
                hover:text-white
              "
            >
              <svg
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="1.8"
                class="h-4 w-4"
              >
                <rect
                  width="17"
                  height="17"
                  x="3.5"
                  y="3.5"
                  rx="4"
                />
                <circle
                  cx="12"
                  cy="12"
                  r="3.5"
                />
                <circle
                  cx="17.5"
                  cy="6.5"
                  r=".7"
                  fill="currentColor"
                  stroke="none"
                />
              </svg>
            </a>

            <!-- LinkedIn -->
            <a
              href="#"
              aria-label="LinkedIn"
              class="
                flex
                h-10
                w-10
                items-center
                justify-center
                rounded-full
                border
                border-gray-700
                bg-gray-800/50
                text-gray-400
                transition
                hover:border-[#2563EB]
                hover:bg-[#2563EB]
                hover:text-white
              "
            >
              <svg
                viewBox="0 0 24 24"
                fill="currentColor"
                class="h-4 w-4"
              >
                <path
                  d="M6.5 8.5H3.25V21H6.5V8.5ZM4.87 3A1.9 1.9 0 1 0 4.87 6.8 1.9 1.9 0 0 0 4.87 3ZM20.75 13.84c0-3.76-2.01-5.51-4.7-5.51-2.17 0-3.14 1.19-3.68 2.03V8.5H9.12V21h3.25v-6.19c0-1.63.31-3.21 2.33-3.21 1.99 0 2.02 1.87 2.02 3.32V21h3.25l.01-7.16Z"
                />
              </svg>
            </a>

            <!-- WhatsApp -->
            <a
              href="https://wa.me/4915560001044"
              target="_blank"
              rel="noopener noreferrer"
              aria-label="WhatsApp"
              class="
                flex
                h-10
                w-10
                items-center
                justify-center
                rounded-full
                border
                border-gray-700
                bg-gray-800/50
                text-gray-400
                transition
                hover:border-[#2563EB]
                hover:bg-[#2563EB]
                hover:text-white
              "
            >
              <svg
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="1.8"
                class="h-4 w-4"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M20.5 11.5a8.5 8.5 0 0 1-12.8 7.35L3 20l1.15-5.2A8.5 8.5 0 1 1 20.5 11.5Z"
                />
              </svg>
            </a>

          </div>
        </div>

        <!-- CONTACT -->
        <div>
          <h3
            class="
              text-sm
              font-semibold
              uppercase
              tracking-wider
              text-white
            "
          >
            Contact
          </h3>

          <div class="mt-6 space-y-5">

            <!-- ADDRESS -->
            <div class="flex gap-4">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="1.8"
                class="mt-0.5 h-5 w-5 shrink-0 text-gray-500"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M15 10.5a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z"
                />
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M19.5 10.5c0 7.142-7.5 10.5-7.5 10.5S4.5 17.642 4.5 10.5a7.5 7.5 0 1 1 15 0Z"
                />
              </svg>

              <p class="text-sm leading-6 text-gray-400">
                Moselle Str. 5,<br />
                38120 Brunswick, Allemagne
              </p>
            </div>

            <!-- EMAIL -->
            <div class="flex gap-4">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="1.8"
                class="mt-0.5 h-5 w-5 shrink-0 text-gray-500"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M3 7.5 12 13l9-5.5"
                />
                <rect
                  width="18"
                  height="15"
                  x="3"
                  y="4.5"
                  rx="2"
                />
              </svg>

              <a
                href="mailto:info@germanjobconnect.de"
                class="text-sm text-gray-400 transition hover:text-white"
              >
                info@germanjobconnect.de
              </a>
            </div>

            <!-- PHONE -->
            <div class="flex gap-4">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="1.8"
                class="mt-0.5 h-5 w-5 shrink-0 text-gray-500"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M6.6 3.8 8.8 3a1.5 1.5 0 0 1 1.8.8l1.1 2.7a1.5 1.5 0 0 1-.4 1.7l-1.5 1.2a11.2 11.2 0 0 0 4.8 4.8l1.2-1.5a1.5 1.5 0 0 1 1.7-.4l2.7 1.1a1.5 1.5 0 0 1 .8 1.8l-.8 2.2a2 2 0 0 1-2 1.3C10.8 18.1 5.9 13.2 5.3 5.8a2 2 0 0 1 1.3-2Z"
                />
              </svg>

              <a
                href="tel:+4915560001044"
                class="text-sm text-gray-400 transition hover:text-white"
              >
                +49 15560001044
              </a>
            </div>

          </div>
        </div>

        <!-- QUICK LINKS -->
        <div>
          <h3
            class="
              text-sm
              font-semibold
              uppercase
              tracking-wider
              text-white
            "
          >
            Liens rapides
          </h3>

          <nav class="mt-6">
            <ul class="space-y-4">

              <li>
                <a
                  href="#"
                  class="text-sm text-gray-400 transition hover:text-white"
                >
                  Maison
                </a>
              </li>

              <li>
                <a
                  href="#services"
                  class="text-sm text-gray-400 transition hover:text-white"
                >
                  Services
                </a>
              </li>

              <li>
                <a
                  href="#candidats"
                  class="text-sm text-gray-400 transition hover:text-white"
                >
                  Candidats
                </a>
              </li>

              <li>
                <a
                  href="#about"
                  class="text-sm text-gray-400 transition hover:text-white"
                >
                  À propos de nous
                </a>
              </li>

              <li>
                <a
                  href="#contact"
                  class="text-sm text-gray-400 transition hover:text-white"
                >
                  Contact
                </a>
              </li>

            </ul>
          </nav>
        </div>

      </div>
    </div>

    <!-- BOTTOM BAR -->
    <div class="border-t border-gray-800">
      <div
        class="
          mx-auto
          flex
          max-w-7xl
          flex-col
          gap-4
          px-6
          py-6
          lg:flex-row
          lg:items-center
          lg:justify-between
          lg:px-8
        "
      >
        <p class="text-xs text-gray-500 sm:text-sm">
          © 2026 Azubiweg. Tous droits réservés.
        </p>

        <div
          class="
            flex
            flex-wrap
            items-center
            gap-x-6
            gap-y-2
            text-xs
            sm:text-sm
          "
        >
          <a
            href="#"
            class="text-gray-500 transition hover:text-white"
          >
            Protection des données
          </a>

          <a
            href="#"
            class="text-gray-500 transition hover:text-white"
          >
            Imprimer
          </a>

          <span class="hidden text-gray-700 sm:inline">
            |
          </span>

          <span class="text-gray-600">
            Conception web par
            <a
              href="#"
              class="font-medium text-gray-400 transition hover:text-white"
            >
              Kolax Studio
            </a>
          </span>
        </div>
      </div>
    </div>

  </footer>
</template>
```
