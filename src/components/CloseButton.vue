<script setup>

    defineProps(['modelValue'])
    const emit = defineEmits(['update:modelValue'])
    
</script>

<template>
    <div class="
            w-5 h-3 relative before:transition-transform before:duration-300 after:transition-transform after:duration-300
            before:absolute before:bg-black dark:before:bg-white before:w-full before:h-[2px]
            after:absolute after:bg-black dark:after:bg-white after:w-full after:h-[2px] after:top-3
            pointer-events-none md:pointer-events-auto 
            "
        :class="modelValue ? 'before:rotate-45 before:translate-y-1.5 after:-rotate-45 after:-translate-y-1.5' : ''"
        @click="emit('update:modelValue', !modelValue)"
    >
    </div>
</template>
