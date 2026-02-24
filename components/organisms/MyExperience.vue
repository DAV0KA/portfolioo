<template>
    <div class="bg-black">
        <div class="flex gap-4 w-full justify-center mt-20 py-20">
            <BaseTitle color="white">My</BaseTitle>
            <BaseTitle color="white" variant="bold">Experience</BaseTitle>
        </div>

        <BaseContainer class="text-white pb-20 flex flex-col gap-10">
            <ExperienceContainer
                v-for="exp in experiences"
                :key="exp.title"
                :logo="exp.logo"
                :title="exp.title"
                :date="exp.date"
                :description="exp.description"
            />
        </BaseContainer>
    </div>
</template>
<script setup>
import BaseTitle from '../atoms/BaseTitle.vue'
import BaseContainer from '../atoms/BaseContainer.vue'
import ExperienceContainer from '../atoms/ExperienceContainer.vue'

const experiences = [
  {
    logo: '/svg/Experience/google.svg',
    title: 'Lead Software Engineer at Google',
    date: 'Nov 2019 - Present',
    description: "As a Senior Software Engineer at Google, I played a pivotal role in developing innovative solutions for Google's core search algorithms. Collaborating with a dynamic team of engineers, I contributed to the enhancement of search accuracy and efficiency, optimizing user experiences for millions of users worldwide."
  },
  {
    logo: '/svg/Experience/youtube.svg',
    title: 'Software Engineer at Youtube',
    date: 'Jan 2017 - Oct 2019',
    description: "At Youtube, I served as a  Software Engineer, focusing on the design and implementation of backend systems for the social media giant's dynamic platform. Working on projects that involved large-scale data processing and user engagement features, I leveraged my expertise to ensure seamless functionality and scalability."
  },
  {
    logo: '/svg/Experience/apple.svg',
    title: 'Junior Software Engineer at Apple',
    date: 'Jan 2016 - Dec 2017',
    description: "During my tenure at Apple, I held the role of Software Architect, where I played a key role in shaping the architecture of mission-critical software projects. Responsible for designing scalable and efficient systems, I provided technical leadership to a cross-functional team."
  }
]
</script>
