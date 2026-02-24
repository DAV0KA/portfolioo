<template>
  <component
    :is="as"
    :class="[
      'tracking-[-0.02em]',
      variant === 'bold' ? 'font-[800]' : 'font-[400]',
      color === 'white' ? 'text-white' : 'text-black',
      'text-4xl 2xl:text-6xl'
    ]"
  >
    <slot />
  </component>
</template>

<script setup>
defineProps({
  as: {
    type: String,
    default: 'h2'
  },
  variant: {
    type: String,
    default: 'regular',
    validator: (v) => ['regular', 'bold'].includes(v)
  },
  color: {
    type: String,
    default: 'black',
    validator: (v) => ['black', 'white'].includes(v)
  }
})
</script>
