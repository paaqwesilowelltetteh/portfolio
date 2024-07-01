<template>
  <div>
    <div class="relative rounded-xl p-6 mb-6 overflow-hidden">
      <div class="absolute inset-0 bg-[url('/tools-logos.jpeg')] bg-cover bg-center"></div>
      <div class="relative z-10">
        <NuxtImg src="/profile-avartar.jpeg" alt="Enoch Tetteh"
          class="ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 bg-gray-200 dark:bg-gray-900 rounded-full h-12 w-12 sm:h-16 sm:w-16"
          sizes="48px sm:64px" placeholder format="webp" />
        <h1 class="text-xl font-bold tracking-tight text-white mt-3">
          Hello, I'm Enoch 👋
        </h1>

      </div>
    </div>
    <div class="mt-9">
      <h1 class="text-xl font-bold tracking-tight text-black mt-3 dark:text-gray-400">
        About Me
      </h1>
      <p class="text-gray-900 dark:text-gray-400">
        I’m a software developer based in Accra, Ghana, specializing in crafting robust web applications using <span
          class="font-bold underline">JavaScript, Nuxt, Vue, and Laravel/PHP</span>. I thrive on both <span
          class="font-bold underline">building initiating projects from scratch and nurturing existing ones to full
          maturity.</span> My passion lies in continually honing my skills and delivering high-quality web solutions.
      </p>
    </div>

  </div>
</template>

<script setup>
useSeoMeta({
  title: "Enoch Tetteh",
  description:
    "I'm Enoch Tetteh, your friendly neighborhood software developer from Accra, Ghana. I specialize in building web applications and sites using Javascript, Nuxt, Vue & Laravel/PHP.",
});
</script>
