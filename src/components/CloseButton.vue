<script setup>
defineProps(['modelValue'])
const emit = defineEmits(['update:modelValue'])
</script>

<template>
    <div class="
        w-5 h-3 relative before:transition-transform before:duration-300 after:transition-transform after:duration-300
        before:absolute before:bg-white before:w-full before:h-[3px]
        after:absolute after:bg-white after:w-full after:h-[3px] after:top-3
    "
    :class="modelValue ? 'before:rotate-45 before:translate-y-1.5 after:-rotate-45 after:-translate-y-1.5' : 'hover:before:rotate-45 hover:before:translate-y-1.5 hover:after:-rotate-45 hover:after:-translate-y-1.5'"
    @click="emit('update:modelValue', !modelValue)"
    >
    </div>
</template>
