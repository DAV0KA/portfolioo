<template>
    <BaseContainer class="flex flex-col-reverse md:flex-row items-center justify-between min-h-[calc(100vh-5rem)]">
        <div class="flex flex-col w-full md:w-1/2">
            <div class="flex flex-col gap-4">
                <div class="flex flex-row gap-4">
                    <BaseTitle>Hello I’am</BaseTitle>
                    <BaseTitle variant="bold">David.</BaseTitle>
                </div>
                <div class="flex flex-row gap-4">
                    <BaseTitle variant="bold">Frontend</BaseTitle>
                    <BaseTitle>Developer</BaseTitle>
                </div>
                <div class="flex flex-row gap-4">
                    <BaseTitle>Based In</BaseTitle>
                    <BaseTitle variant="bold">RUSSIA.</BaseTitle>
                </div>
            </div>

            <BaseText class=" pt-10">I'm Evren Shah Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to specimen book.</BaseText>

            <div class="flex gap-5 pt-10 justify-between md:justify-start">
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
        </div>

        <img class="mt-10 md:-ml-20 md:mt-20 mb-10 md:mr-20 -z-10 w-full md:w-1/2 min-h-20" src="/svg/men.svg" alt="men">
    </BaseContainer>
</template>
<script setup>
import BaseContainer from '../atoms/BaseContainer.vue'
import BaseTitle from '../atoms/BaseTitle.vue'
import BaseText from '../atoms/BaseText.vue'
import BaseButton from '../atoms/BaseButton.vue'
</script>