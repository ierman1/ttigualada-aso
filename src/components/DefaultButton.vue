<script setup lang="ts">

defineEmits(['clicked'])

defineProps<{
    type: string,
    href?: string,
    variant?: 'filled' | 'outlined'
}>()

</script>

<template>
    <button
        v-if="type === 'button'"
        @click="$emit('clicked')"
        :class="[
            'modern-antiqua-regular py-2 px-4 rounded drop-shadow-sm cursor-pointer transition-colors',
            variant === 'outlined' 
                ? 'border border-teal-500 text-teal-500 bg-transparent hover:bg-teal-500 hover:text-white'
                : 'bg-teal-500 text-white hover:bg-teal-600'
        ]"
    >
        <slot />
    </button>
    
    <a 
        v-else-if="type === 'link'"
        :href="href"
        :class="[
            'inline-block modern-antiqua-regular py-2 px-4 rounded drop-shadow-sm cursor-pointer transition-colors',
            variant === 'outlined' 
                ? 'border border-teal-500 text-teal-500 bg-transparent hover:bg-teal-500 hover:text-white'
                : 'bg-teal-500 text-white hover:bg-teal-600'
        ]"
    >
        <slot />
    </a>
</template>