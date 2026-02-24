<template>
    <BaseContainer id="about" class="flex flex-col md:flex-row gap-10 md:gap-20 py-20">
        <img class="md:w-1/2" src="/svg/men2.svg" alt="men2">

        <div>
            <div class="flex gap-4 w-full py-2">
                <BaseTitle>About</BaseTitle>
                <BaseTitle variant="bold">Me</BaseTitle> 
            </div>
            <BaseText class=" pt-10">I'm a passionate, self-proclaimed designer who specializes in full stack development (React.js & Node.js). I am very enthusiastic about bringing the technical and visual aspects of digital products to life. User experience, pixel perfect design, and writing clear, readable, highly performant code matters to me.</BaseText>
            <BaseText class=" pt-5">I began my journey as a web developer in 2015, and since then, I've continued to grow and evolve as a developer, taking on new challenges and learning the latest technologies along the way. Now, in my early thirties, 7 years after starting my web development journey, I'm building cutting-edge web applications using modern technologies such as Next.js, TypeScript, Nestjs, Tailwindcss, Supabase and much more.</BaseText>
            <BaseText class=" pt-5">When I'm not in full-on developer mode, you can find me hovering around on twitter or on indie hacker, witnessing the journey of early startups or enjoying some free time. You can follow me on Twitter where I share tech-related bites and build in public, or you can follow me on GitHub.</BaseText>
        </div>
    </BaseContainer>
    
    
</template>
<script setup>
import BaseTitle from '../atoms/BaseTitle.vue'
import BaseText from '../atoms/BaseText.vue'
import BaseContainer from '../atoms/BaseContainer.vue'
</script>