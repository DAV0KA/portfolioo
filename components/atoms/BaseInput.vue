<template>
  <component
    :is="isTextarea ? 'textarea' : 'input'"
    :value="modelValue"
    @input="onInput"
    v-bind="$attrs"
    :class="[
      'w-full border-2 border-black rounded px-4 py-3 outline-none transition-all duration-200',
      'placeholder:text-gray-400',
      'focus:ring-2 focus:ring-black/20 focus:scale-[1.01]',
      isTextarea ? 'resize-none min-h-[120px]' : ''
    ]"
  />
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  modelValue: {
    type: [String, Number],
    default: ''
  },
  variant: {
    type: String,
    default: 'input'
  }
})

const emit = defineEmits(['update:modelValue'])

const isTextarea = computed(() => props.variant === 'textarea')

const onInput = (e) => {
  emit('update:modelValue', e.target.value)
}
</script>