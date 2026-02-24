<template>
  <BaseContainer id="contact" class="my-20 flex flex-col md:flex-row justify-between gap-10">
    <form
      @submit.prevent="handleSubmit"
      class="flex flex-col gap-5 w-full mr-20"
    >
      <BaseInput
        v-model="form.name"
        placeholder="Your name"
      />

      <BaseInput
        v-model="form.email"
        type="email"
        placeholder="Email"
      />

      <BaseInput
        v-model="form.website"
        placeholder="Your website (If exists)"
      />

      <BaseInput
        v-model="form.message"
        variant="textarea"
        placeholder="How can I help?*"
      />

      <p v-if="error" class="text-red-500 text-sm">
        {{ error }}
      </p>

      <div class="flex gap-5 flex-wrap items-center">
        <BaseButton
            type="submit"
            :disabled="loading"
            >
            {{
                loading
                ? 'Sending...'
                : success
                    ? 'Message sent'
                    : 'Get In Touch'
            }}
        </BaseButton>

        <BaseButton class="hover:scale-110">
            <img class="group-hover:scale-150 transition-transform" src="/svg/Social/Social icon.svg" alt="1">
        </BaseButton>
        <BaseButton class="hover:scale-110" variant="white">
            <img class="group-hover:scale-150 transition-transform" src="/svg/Social/Social icon (1).svg" alt="1">
        </BaseButton>
        <BaseButton class="hover:scale-110" variant="white">
            <img class="group-hover:scale-150 transition-transform" src="/svg/Social/Social icon (2).svg" alt="1">
        </BaseButton>
        <BaseButton class="hover:scale-110" variant="white">
            <img class="group-hover:scale-150 transition-transform" src="/svg/Social/Social icon (3).svg" alt="1">
        </BaseButton>
      </div>
    </form>

    <div class="flex flex-col gap-1 md:gap-4">
        <div class="flex flex-row gap-4">
            <BaseTitle variant="bold">Let’s</BaseTitle>
            <BaseTitle>talk</BaseTitle>
            <BaseTitle variant="bold">for</BaseTitle>
        </div>
        <div class="flex flex-row gap-4">
            <BaseTitle variant="bold">Something special</BaseTitle>
        </div>

    <BaseText class="my-2">I seek to push the limits of creativity to create high-engaging, user-friendly, and memorable interactive experiences.</BaseText>

    <div class="text-xl md:text-2xl xl:text-3xl text-black">Youremail@gmail.com</div>

    </div>


  </BaseContainer>
</template>

<script setup>
import { reactive, ref } from 'vue'
import BaseContainer from '../atoms/BaseContainer.vue'
import BaseButton from '../atoms/BaseButton.vue'
import BaseInput from '../atoms/BaseInput.vue'
import BaseTitle from '../atoms/BaseTitle.vue'
import BaseText from '../atoms/BaseText.vue'

const form = reactive({
  name: '',
  email: '',
  website: '',
  message: ''
})

const loading = ref(false)
const error = ref('')
const success = ref(false)

const handleSubmit = async () => {
  error.value = ''
  success.value = false

  if (!form.name || !form.email || !form.message) {
    error.value = 'Please fill required fields.'
    return
  }

  loading.value = true

  try {
    await fetch('https://jsonplaceholder.typicode.com/posts', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify(form)
    })

    success.value = true

    if (success.value) {
        setTimeout(() => {
        success.value = false
    }, 3000)}

    form.name = ''
    form.email = ''
    form.website = ''
    form.message = ''

  } catch (e) {
    error.value = 'Something went wrong.'
  } finally {
    loading.value = false
  }
}
</script>