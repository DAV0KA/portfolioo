<template>
  <div class="border border-gray-500 text-white p-8 rounded-xl flex gap-6 items-start">

    <div class="flex flex-col gap-3">
      <!-- Заголовок + дата -->
      <div class="flex flex-col md:flex-row md:items-center md:justify-between gap-2">
        <div class="flex gap-5 items-center">
            <!-- Лого -->
            <img 
                v-if="logo" 
                :src="logo" 
                alt="company logo"
                class="w-7 h-7 object-contain"
            />

            <h3 class="text-xl font-semibold">
            {{ title }}
            </h3>
        </div>

        <span class="text-sm text-gray-400 py-2 md:py-0">
          {{ date }}
        </span>
      </div>

      <!-- Текст -->
      <p class="text-gray-300 leading-relaxed pt-0 md:pt-3">
        {{ description }}
      </p>

    </div>
  </div>
</template>

<script setup>
defineProps({
  logo: String,
  title: {
    type: String,
    required: true
  },
  date: String,
  description: String
})
</script>
