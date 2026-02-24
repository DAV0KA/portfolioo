<template>
  <button
    :class="[
      'px-3 py-3 rounded font-medium transition',
      variantClass
    ]"
    class="group transition-transform"
  >
    <slot />
  </button>
</template>

<script setup>
const props = defineProps({
  variant: {
    type: String,
    default: 'black', // 'black' | 'white'
    validator: (v) => ['black', 'white'].includes(v)
  }
})

const variantClass = {
  black: 'bg-black text-white',
  white: 'bg-white text-black border-2 border-black'
}[props.variant]
</script>
