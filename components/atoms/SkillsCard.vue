<template>
  <div class="w-full bg-white border-2 border-black rounded-lg p-5 flex flex-col items-center gap-4">
    
    <img
      v-if="image"
      :src="image"
      alt=""
      class="w-15 object-cover rounded-md"
    />

    <p class="text-center font-bold text-black">
      <slot />
    </p>

  </div>
</template>

<script setup>
defineProps({
  image: {
    type: String,
    default: ''
  }
})
</script>
