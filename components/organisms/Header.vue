<template>
  <header class="w-full py-4 h-20">
    <BaseContainer class="flex items-center justify-between">
      
      <!-- Логотип -->
      <div class="text-xl font-bold tracking-[-0.02em]">
        Logo
      </div>

      <!-- Навигация -->
      <nav class="flex items-center gap-8 text-sm">
        <a href="#about" class="font-semibold hover:text-gray-600">About Me</a>
        <a href="#skills" class="font-semibold hover:text-gray-600">Skills</a>
        <a href="#projects" class="font-semibold hover:text-gray-600">Project</a>
        <a href="#contact" class="font-semibold hover:text-gray-600">Contact me</a>
      </nav>

      <!-- Кнопка -->
      <BaseButton class="flex gap-3">
        Resume
        <svg class="group-hover:scale-125 transition-transform" width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M17.5 12.5V13.5C17.5 14.9001 17.5 15.6002 17.2275 16.135C16.9878 16.6054 16.6054 16.9878 16.135 17.2275C15.6002 17.5 14.9001 17.5 13.5 17.5H6.5C5.09987 17.5 4.3998 17.5 3.86502 17.2275C3.39462 16.9878 3.01217 16.6054 2.77248 16.135C2.5 15.6002 2.5 14.9001 2.5 13.5V12.5M14.1667 8.33333L10 12.5M10 12.5L5.83333 8.33333M10 12.5V2.5" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </BaseButton>

    </BaseContainer>
  </header>
</template>

<script setup>
import BaseContainer from '../atoms/BaseContainer.vue'
import BaseButton from '../atoms/BaseButton.vue'
</script>
