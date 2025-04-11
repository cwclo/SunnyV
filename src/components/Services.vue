<template>
  <section class="grid md:grid-cols-2">
    <!-- Block 1: Text Left, Image Right -->
    <FadeInSection>
      <div class="flex flex-col justify-center items-center text-center px-6 py-20 md:py-32 bg-white">
        <div class="max-w-md">
          <h2 class="text-3xl md:text-4xl font-extrabold text-gray-800 mb-6">Transform your brand</h2>
          <p class="text-gray-500 mb-6">
            We are a full-service creative agency specializing in helping brands grow fast. Engage your clients through
            compelling visuals that do most of the marketing for you.
          </p>
          <a href="#" class="uppercase text-yellow-400 font-bold tracking-wider border-b-4 border-yellow-300 hover:border-yellow-500">
            Learn more
          </a>
        </div>
      </div>
    </FadeInSection>
    <div class="h-96 md:h-auto bg-[url('/images/desktop/image-transform.jpg')] bg-cover bg-center"></div>

    <!-- Block 2: Image Left, Text Right -->
    <div class="h-96 md:h-auto bg-[url('/images/desktop/image-stand-out.jpg')] bg-cover bg-center order-1 md:order-none"></div>
    <FadeInSection>
      <div class="flex flex-col justify-center items-center text-center px-6 py-20 md:py-32 bg-white">
        <div class="max-w-md">
          <h2 class="text-3xl md:text-4xl font-extrabold text-gray-800 mb-6">Stand out to the right audience</h2>
          <p class="text-gray-500 mb-6">
            Using a collaborative formula of designers, researchers, photographers, videographers, and copywriters, we’ll
            build and extend your brand in digital places.
          </p>
          <a href="#" class="uppercase text-pink-400 font-bold tracking-wider border-b-4 border-pink-300 hover:border-pink-500">
            Learn more
          </a>
        </div>
      </div>
    </FadeInSection>
  </section>
</template>

<script setup>
import FadeInSection from './FadeInSection.vue'
</script>
