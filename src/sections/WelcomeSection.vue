<script setup lang="ts">
import DefaultButton from '../components/DefaultButton.vue';

</script>

<template>
    <section class="py-12">
        <div class="container mx-auto px-4 flex flex-col lg:flex-row items-baseline lg:gap-8">
            <h1 class="text-4xl md:text-6xl mb-4 modern-antiqua-regular">Welcome to your tabletop gaming haven!</h1>
            <div>
                <p class="text-lg modern-antiqua-regular">Join us for an exciting adventure in tabletop gaming! From Magic: The Gathering to Dungeons & Dragons, we provide a welcoming space for players of all levels.</p>
                <DefaultButton type="link" href="/reserve" class="mt-4">
                    Reserve a table
                </DefaultButton>
            </div>
        </div>
    </section>
</template>