<template>
  <div
    :class="[
      'rounded-2xl p-8 flex flex-col gap-6 shadow-lg transition-all',
      isDark ? 'bg-black text-white' : 'bg-white text-black'
    ]"
  >
    <div class="relative w-20 h-20 mx-auto">
      <img
        v-if="logo"
        :src="logo"
        alt="company logo"
        :class="[
          'w-20 h-20 rounded-full object-cover border-2',
          isDark ? 'border-white' : 'border-black'
        ]"
      />
    </div>

    <p class="mx-auto" :class="isDark ? 'text-white' : 'text-black'">
      {{ text }}
    </p>

    <div
        :class="[
            'w-1/2 h-[2px] rounded-xl mx-auto',
            isDark ? 'bg-white' : 'bg-black'
        ]"
    />

    <div class="flex flex-col mx-auto">
      <span class="font-semibold">
        {{ name }}
      </span>
      <span :class="isDark ? 'text-gray-400' : 'text-gray-500'" class="text-sm">
        {{ position }}
      </span>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  logo: String,
  text: { type: String, required: true },
  name: { type: String, required: true },
  position: String,
  variant: {
    type: String,
    default: 'light'
  }
})

const isDark = computed(() => props.variant === 'dark')
</script>
