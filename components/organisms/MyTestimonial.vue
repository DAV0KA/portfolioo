<template>
    <div class="flex gap-4 w-full justify-center py-5">
        <BaseTitle>My</BaseTitle>
        <BaseTitle variant="bold">Testimonial</BaseTitle> 
    </div>

    <BaseContainer class="py-20 grid grid-cols-1 md:grid-cols-3 gap-8">
        <TestimonialCard
            v-for="item in testimonials"
            :key="item.name + item.position"
            :logo="item.logo"
            :text="item.text"
            :name="item.name"
            :position="item.position"
            :variant="item.variant"
        />
    </BaseContainer>

</template>
<script setup>
import BaseTitle from '../atoms/BaseTitle.vue'
import BaseContainer from '../atoms/BaseContainer.vue'
import TestimonialCard from '../atoms/TestimonialCard.vue'

const testimonials = [
  {
    logo: '/img/Testimonial/cat.png',
    text: 'Храни тебя бог',
    name: 'Екатерина Радченко',
    position: 'Developer at Rubezh',
    variant: 'light'
  },
  {
    logo: '/img/Testimonial/cat.png',
    text: 'я не буду... ты будешь',
    name: 'Екатерина Радченко',
    position: 'Developer at Rubezh',
    variant: 'dark'
  },
  {
    logo: '/img/Testimonial/cat.png',
    text: 'Надеюсь он не пожимает руки с утра всем',
    name: 'Екатерина Радченко',
    position: 'Developer at Rubezh',
    variant: 'light'
  }
]
</script>