<template>
  <div class="group w-full bg-white border-2 border-black rounded-lg p-5 flex flex-col items-center gap-4
          transition-all duration-300 ease-out
          hover:-translate-y-2 hover:shadow-xl">
    <img
      v-if="image"
      :src="image"
      alt=""
      class="w-15 object-cover rounded-md transition-transform duration-300 ease-out
            group-hover:scale-125"
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
