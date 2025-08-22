<script setup lang="ts">

defineEmits(['clicked'])

defineProps<{
    type: string,
    href?: string
}>()

</script>

<template>
    <button
        v-if="type === 'button'"
        @click="$emit('clicked')"
        class="bg-teal-500 modern-antiqua-regular text-white py-2 px-4 rounded hover:bg-teal-600 drop-shadow-sm cursor-pointer"
    >
        <slot />
    </button>
    
    <a 
        v-else-if="type === 'link'"
        :href="href"
        class="inline-block bg-teal-500 modern-antiqua-regular text-white py-2 px-4 rounded hover:bg-teal-600 drop-shadow-sm cursor-pointer"
    >
        <slot />
    </a>
</template>