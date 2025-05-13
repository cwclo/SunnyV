<template>
  <header
    class="absolute top-0 left-0 w-full z-50 px-6 md:px-12 py-8 flex justify-between items-center"
  >
    <!-- Logo -->
    <img src="/images/logo.svg" alt="Sunnyside Logo" class="w-32 md:w-40" />

    <!-- Desktop Nav -->
    <nav
      class="hidden md:flex space-x-10 items-center text-white font-semibold"
    >
      <NavLink href="#about">About</NavLink>
      <NavLink href="#services">Services</NavLink>
      <NavLink href="#projects">Projects</NavLink>
      <a
        href="#contact"
        class="bg-white text-black px-6 py-2 uppercase rounded-full text-sm hover:bg-opacity-80 transition duration-300"
      >
        Contact
      </a>
    </nav>


    <!-- Mobile Hamburger -->
    <button @click="toggleMenu" class="md:hidden z-50 relative">
      <img src="/images/icon-hamburger.svg" alt="Menu" class="w-6 h-6" />
    </button>

    <!-- Overlay to close on outside click -->
    <div
      v-if="isOpen"
      class="fixed inset-0 bg-black/30 z-30"
      @click="closeMenu"
    ></div>

    <!-- Mobile Slide-In Menu -->
    <transition name="slide">
      <div
        v-if="isOpen"
        class="fixed top-0 right-0 w-2/3 h-full bg-white text-[#2c7566] flex flex-col items-center justify-center gap-8 font-semibold text-lg shadow-2xl z-40"
      >
        <!-- Close Button -->
        <button
          @click="closeMenu"
          class="absolute top-6 right-6 text-[#2c7566] hover:text-yellow-400 z-50"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-8 w-8"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>

        <!-- Mobile Links -->
        <NavLink
          href="#about"
          @click="closeMenu"
          baseColor="text-[#2c7566]"
          underlineColor="bg-[#2c7566]"
          activeClass="text-yellow-500"
        >
          About
        </NavLink>

        <NavLink
          href="#services"
          @click="closeMenu"
          baseColor="text-[#2c7566]"
          underlineColor="bg-[#2c7566]"
          activeClass="text-yellow-500"
        >
          Services
        </NavLink>

        <NavLink
          href="#projects"
          @click="closeMenu"
          baseColor="text-[#2c7566]"
          underlineColor="bg-[#2c7566]"
          activeClass="text-yellow-500"
        >
          Projects
        </NavLink>

        <a
          href="#contact"
          @click="closeMenu"
          class="bg-yellow-400 text-white px-6 py-2 uppercase rounded-full text-sm hover:bg-yellow-500"
        >
          Contact
        </a>
      </div>
    </transition>
  </header>
</template>

<script setup>
import { ref } from "vue";
import NavLink from "./NavLink.vue";

const isOpen = ref(false);

function toggleMenu() {
  isOpen.value = !isOpen.value;
}

function closeMenu() {
  isOpen.value = false;
}
</script>

<style scoped>
.slide-enter-active,
.slide-leave-active {
  transition: transform 0.3s ease;
}
.slide-enter-from {
  transform: translateX(100%);
}
.slide-enter-to {
  transform: translateX(0%);
}
.slide-leave-from {
  transform: translateX(0%);
}
.slide-leave-to {
  transform: translateX(100%);
}
</style>
