```vue
<template>
  <section
    id="contact"
    class="relative overflow-hidden bg-[#F9FAFB] py-20 sm:py-24 lg:py-28"
  >
    <div class="mx-auto max-w-7xl px-6 lg:px-8">

      <!-- HEADER -->
      <div class="mx-auto max-w-2xl text-center">
        <span
          class="inline-flex items-center rounded-full bg-blue-50 px-4 py-2 text-sm font-semibold text-[#2563EB]"
        >
          Contact
        </span>

        <h2
          class="mt-5 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl lg:text-5xl"
        >
          Contactez-nous
        </h2>

        <p
          class="mt-5 text-base leading-7 text-gray-600 sm:text-lg"
        >
          Nous sommes là pour répondre à vos questions.
        </p>
      </div>

      <!-- CONTENT -->
      <div
        class="mx-auto mt-14 grid max-w-6xl gap-8 lg:grid-cols-[1.1fr_0.9fr]"
      >

        <!-- FORM CARD -->
        <div
          class="rounded-3xl border border-gray-200 bg-white p-6 shadow-sm sm:p-8 lg:p-10"
        >
          <div class="mb-8">
            <h3 class="text-xl font-bold text-gray-900">
              Envoyez-nous un message
            </h3>

            <p class="mt-2 text-sm leading-6 text-gray-500">
              Remplissez le formulaire et notre équipe vous répondra dans les
              meilleurs délais.
            </p>
          </div>

          <form class="space-y-6">

            <!-- NAME -->
            <div>
              <label
                for="name"
                class="mb-2 block text-sm font-semibold text-gray-900"
              >
                Nom
              </label>

              <input
                id="name"
                type="text"
                name="name"
                placeholder="Votre nom"
                class="
                  block
                  w-full
                  rounded-xl
                  border
                  border-gray-300
                  bg-white
                  px-4
                  py-3.5
                  text-sm
                  text-gray-900
                  outline-none
                  placeholder:text-gray-400
                  transition
                  focus:border-[#2563EB]
                  focus:ring-4
                  focus:ring-blue-100
                "
              />
            </div>

            <!-- EMAIL -->
            <div>
              <label
                for="email"
                class="mb-2 block text-sm font-semibold text-gray-900"
              >
                E-mail
              </label>

              <input
                id="email"
                type="email"
                name="email"
                placeholder="votre@email.com"
                class="
                  block
                  w-full
                  rounded-xl
                  border
                  border-gray-300
                  bg-white
                  px-4
                  py-3.5
                  text-sm
                  text-gray-900
                  outline-none
                  placeholder:text-gray-400
                  transition
                  focus:border-[#2563EB]
                  focus:ring-4
                  focus:ring-blue-100
                "
              />
            </div>

            <!-- PHONE -->
            <div>
              <label
                for="phone"
                class="mb-2 block text-sm font-semibold text-gray-900"
              >
                Téléphone
              </label>

              <input
                id="phone"
                type="tel"
                name="phone"
                placeholder="+49 ..."
                class="
                  block
                  w-full
                  rounded-xl
                  border
                  border-gray-300
                  bg-white
                  px-4
                  py-3.5
                  text-sm
                  text-gray-900
                  outline-none
                  placeholder:text-gray-400
                  transition
                  focus:border-[#2563EB]
                  focus:ring-4
                  focus:ring-blue-100
                "
              />
            </div>

            <!-- MESSAGE -->
            <div>
              <label
                for="message"
                class="mb-2 block text-sm font-semibold text-gray-900"
              >
                Message
              </label>

              <textarea
                id="message"
                name="message"
                rows="6"
                placeholder="Comment pouvons-nous vous aider ?"
                class="
                  block
                  w-full
                  resize-none
                  rounded-xl
                  border
                  border-gray-300
                  bg-white
                  px-4
                  py-3.5
                  text-sm
                  leading-6
                  text-gray-900
                  outline-none
                  placeholder:text-gray-400
                  transition
                  focus:border-[#2563EB]
                  focus:ring-4
                  focus:ring-blue-100
                "
              ></textarea>
            </div>

            <!-- CONSENT -->
            <div class="flex items-start gap-3">
              <input
                id="privacy"
                type="checkbox"
                class="
                  mt-1
                  h-4
                  w-4
                  shrink-0
                  rounded
                  border-gray-300
                  text-[#2563EB]
                  focus:ring-[#2563EB]
                "
              />

              <label
                for="privacy"
                class="text-xs leading-5 text-gray-500"
              >
                En soumettant ce formulaire, vous acceptez le traitement de
                vos données conformément à notre
                <a
                  href="#"
                  class="font-medium text-[#2563EB] transition hover:underline"
                >
                  politique de confidentialité
                </a>.
              </label>
            </div>

            <!-- BUTTON -->
            <button
              type="submit"
              class="
                inline-flex
                w-full
                items-center
                justify-center
                gap-2
                rounded-xl
                bg-[#2563EB]
                px-6
                py-3.5
                text-sm
                font-semibold
                text-white
                shadow-sm
                transition-all
                duration-200
                hover:bg-blue-700
                hover:shadow-lg
                focus:outline-none
                focus:ring-4
                focus:ring-blue-200
                active:scale-[0.99]
              "
            >
              Envoyer un message

              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                class="h-4 w-4"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M4.5 19.5 19.5 4.5m0 0H8.25m11.25 0v11.25"
                />
              </svg>
            </button>

          </form>
        </div>

        <!-- CONTACT DETAILS -->
        <div class="flex flex-col gap-6">

          <!-- INTRO CARD -->
          <div
            class="rounded-3xl bg-[#2563EB] p-7 text-white shadow-sm sm:p-8"
          >
            <p class="text-sm font-semibold text-blue-100">
              Parlons de votre projet
            </p>

            <h3
              class="mt-3 text-2xl font-bold tracking-tight sm:text-3xl"
            >
              Nous sommes à votre écoute.
            </h3>

            <p
              class="mt-4 text-sm leading-6 text-blue-100 sm:text-base"
            >
              Une question, un projet ou besoin d'un accompagnement ?
              Contactez notre équipe directement.
            </p>
          </div>

          <!-- DETAILS -->
          <div
            class="rounded-3xl border border-gray-200 bg-white p-7 shadow-sm sm:p-8"
          >
            <h3 class="text-xl font-bold text-gray-900">
              Coordonnées
            </h3>

            <div class="mt-7 space-y-7">

              <!-- ADDRESS -->
              <div class="flex gap-4">
                <div
                  class="
                    flex
                    h-11
                    w-11
                    shrink-0
                    items-center
                    justify-center
                    rounded-xl
                    bg-blue-50
                    text-[#2563EB]
                  "
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="1.8"
                    class="h-5 w-5"
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
                </div>

                <div>
                  <p class="text-sm font-semibold text-gray-900">
                    Adresse
                  </p>

                  <p class="mt-1 text-sm leading-6 text-gray-500">
                    Moselle Str. 5,<br />
                    38120 Brunswick, Allemagne
                  </p>
                </div>
              </div>

              <!-- EMAIL -->
              <div class="flex gap-4">
                <div
                  class="
                    flex
                    h-11
                    w-11
                    shrink-0
                    items-center
                    justify-center
                    rounded-xl
                    bg-blue-50
                    text-[#2563EB]
                  "
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="1.8"
                    class="h-5 w-5"
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
                </div>

                <div>
                  <p class="text-sm font-semibold text-gray-900">
                    E-mail
                  </p>

                  <a
                    href="mailto:info@germanjobconnect.de"
                    class="
                      mt-1
                      block
                      text-sm
                      text-gray-500
                      transition
                      hover:text-[#2563EB]
                    "
                  >
                    info@germanjobconnect.de
                  </a>
                </div>
              </div>

              <!-- WHATSAPP -->
              <div class="flex gap-4">
                <div
                  class="
                    flex
                    h-11
                    w-11
                    shrink-0
                    items-center
                    justify-center
                    rounded-xl
                    bg-blue-50
                    text-[#2563EB]
                  "
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="1.8"
                    class="h-5 w-5"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M21 11.5a8.5 8.5 0 0 1-12.8 7.35L3 20l1.15-5.2A8.5 8.5 0 1 1 21 11.5Z"
                    />
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M8.5 9.5c.2-.4.4-.4.7-.4h.4c.2 0 .4.1.5.4l.7 1.5c.1.2.1.4-.1.6l-.5.6c.6 1.1 1.5 2 2.6 2.6l.6-.5c.2-.2.4-.2.6-.1l1.5.7c.3.1.4.3.4.5v.4c0 .3 0 .5-.4.7-.4.2-1 .3-1.5.2-2.7-.6-5.8-3.7-6.4-6.4-.1-.5 0-1.1.2-1.5Z"
                    />
                  </svg>
                </div>

                <div>
                  <p class="text-sm font-semibold text-gray-900">
                    WhatsApp
                  </p>

                  <a
                    href="https://wa.me/4915560001044"
                    target="_blank"
                    rel="noopener noreferrer"
                    class="
                      mt-1
                      block
                      text-sm
                      text-gray-500
                      transition
                      hover:text-[#2563EB]
                    "
                  >
                    +49 15560001044
                  </a>
                </div>
              </div>

            </div>
          </div>

          <!-- FREE CONSULTATION -->
          <div
            class="rounded-3xl border border-blue-100 bg-blue-50 p-6 sm:p-7"
          >
            <div class="flex items-start gap-4">

              <div
                class="
                  flex
                  h-11
                  w-11
                  shrink-0
                  items-center
                  justify-center
                  rounded-xl
                  bg-white
                  text-[#2563EB]
                  shadow-sm
                "
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="1.8"
                  class="h-5 w-5"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M12 3v18m9-9H3"
                  />
                </svg>
              </div>

              <div>
                <h4 class="font-semibold text-gray-900">
                  Consultation gratuite
                </h4>

                <p class="mt-1 text-sm leading-6 text-gray-600">
                  Consultation gratuite et sans engagement pour échanger
                  sur votre projet et vos besoins.
                </p>
              </div>

            </div>
          </div>

        </div>
      </div>
    </div>
  </section>
</template>
```
