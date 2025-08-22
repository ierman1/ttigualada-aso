<script setup lang="ts">

defineProps<{
    event: {
        title: string,
        date: string,
        description: string
    }
}>()

</script>

<template>
    <div class="border-b-2 border-stone-500 py-8 text-left flex items-center modern-antiqua-regular">
        <img 
            src="https://placehold.co/150x150"
            alt="Event Image"
            class="object-cover rounded-xl mr-6"
        />
        <div>
            <h3 class="text-2xl lg:text-3xl font-semibold mb-1">{{ event.title }}</h3>
            <p class="text-sm mb-4">{{ event.date }}</p>
            <p>{{ event.description }}</p>
        </div>
    </div>
</template>