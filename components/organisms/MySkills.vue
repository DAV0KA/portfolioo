<template>
  <div class="flex gap-4 w-full justify-center">
    <BaseTitle>My</BaseTitle>
    <BaseTitle variant="bold">Skills</BaseTitle>
  </div>

    <BaseContainer class="grid grid-cols-4 gap-5 py-12">
    <SkillsCard v-for="skill in skills" :key="skill.name" :image="skill.image">
        {{ skill.name }}
    </SkillsCard>
    </BaseContainer>

</template>

<script setup>
import BaseTitle from '../atoms/BaseTitle.vue'
import BaseContainer from '../atoms/BaseContainer.vue'
import SkillsCard from '../atoms/SkillsCard.vue'

const skills = [
    { name: 'Git', image: '../svg/skills/1.svg' },
    { name: 'Nest.Js', image: '../svg/skills/2.svg' },
    { name: 'Sass/scss', image: '../svg/skills/3.svg' },
    { name: 'Storybook', image: '../svg/skills/4.svg' },
    { name: 'Git', image: '../svg/skills/1.svg' },
    { name: 'Nest.Js', image: '../svg/skills/2.svg' },
    { name: 'Sass/scss', image: '../svg/skills/3.svg' },
    { name: 'Storybook', image: '../svg/skills/4.svg' },
  
]
</script>
