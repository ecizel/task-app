<script setup>

    defineProps(['msg','path'])

</script>

<template>
    <a class="
            py-2 text-sm sm:text-base hover:text-green-500 transition-colors duration-300 relative w-fit
            before:absolute before:bg-green-500 before:w-0 before:h-px before:bottom-1.5 before:left-1/2
            hover:before:w-full hover:before:left-0 before:transition-all before:duration-300
            " 
        v-text="msg"
        :href="path"></a>
</template>