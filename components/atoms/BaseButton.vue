<template>
  <button
    :type="type"
    :disabled="disabled"
    :class="[
      'group px-4 py-3 rounded-lg font-medium transition-all duration-200 ease-out',
      'focus:outline-none focus:ring-2 focus:ring-black/30',
      'disabled:opacity-50 disabled:cursor-not-allowed',
      variantClass
    ]"
  >
    <slot />
  </button>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  variant: {
    type: String,
    default: 'black',
    validator: v => ['black', 'white'].includes(v)
  },
  type: {
    type: String,
    default: 'button'
  },
  disabled: {
    type: Boolean,
    default: false
  }
})

const variantClass = computed(() => {
  return {
    black:
      'bg-black text-white active:scale-95',
    white:
      'bg-white text-black border-2 border-black hover:text-white active:scale-95'
  }[props.variant]
})
</script>