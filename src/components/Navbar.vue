<script setup>
    import { ref } from 'vue'
    import ButtonBefore from './ButtonBefore.vue'
    import CloseButton from './CloseButton.vue'

    const dropbarOn = ref(false)

</script>

<template>
    <!-- navbar -->
    <div 
        class="sticky flex w-screen sm:w-[90vw] sm:h-10 sm:rounded-b-lg place-self-center bg-slate-900/70 backdrop-blur-[1px] sm:border-b border-green-500 px-5 sm:px-8 justify-between items-center">
        <ButtonBefore msg="Task-app" path="#"/>
        <div class="hidden sm:flex gap-8 sm:gap-[10vw]">
            <ButtonBefore msg="Home" path="#"/>
            <ButtonBefore  msg="Other projects" path="#"/>
        </div>
        <div class="sm:hidden">
            <CloseButton v-model="dropbarOn"/>
        </div>
    </div>

    <!-- dropbar -->
    <div class="sticky sm:hidden px-5 flex flex-col bg-slate-900/70 border-b border-b-green-500 overflow-auto transition-all duration-300"
         :class="dropbarOn ? 'h-20' : 'h-0'">
        <ButtonBefore msg="Home" path="#"/>
        <ButtonBefore msg="Other projects" path="#"/>
    </div>

    
</template>
