<template>
    <a
      :href="href"
      class="group relative inline-block"
      :class="[
        baseColor,
        isActive ? activeClass : '',
      ]"
    >
      <span><slot /></span>
      <span
        class="absolute left-0 bottom-0 w-0 h-[2px] transition-all duration-300 group-hover:w-full"
        :class="underlineColor"
      ></span>
    </a>
  </template>
  
  <script setup>
  import { ref, onMounted, onUnmounted } from 'vue'
  
  const props = defineProps({
    href: String,
    baseColor: {
      type: String,
      default: 'text-white'
    },
    activeClass: {
      type: String,
      default: 'font-bold'
    },
    underlineColor: {
      type: String,
      default: 'bg-white'
    }
  })
  
  const isActive = ref(false)
  
  onMounted(() => {
    const sectionId = props.href?.replace('#', '')
    const section = document.getElementById(sectionId)
  
    if (section) {
      const observer = new IntersectionObserver(
        ([entry]) => {
          isActive.value = entry.isIntersecting
        },
        { threshold: 0.6 }
      )
      observer.observe(section)
      onUnmounted(() => observer.disconnect())
    }
  })
  </script>
  