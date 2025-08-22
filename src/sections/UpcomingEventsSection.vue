<script setup lang="ts">
import DefaultButton from '@/components/DefaultButton.vue'
import EventCard from '@/components/EventCard.vue'
import { ref } from 'vue'

const events = ref([
    {
        title: "Magic Tournament",
        date: "Fri 09 Feb 2024",
        description: "Join us for an epic Magic the Gathering tournament with prizes and fun for everyone!"
    },
    {
        title: "D&D Game Night",
        date: "Sat 10 Feb 2024",
        description: "Gather your friends for an unforgettable Dungeons & Dragons game night filled with adventure!"
    },
    {
        title: "Expansion Release",
        date: "Sun 11 Feb 2024",
        description: "Celebrate the latest Magic the Gathering expansion with friends and new players alike!"
    }
])

</script>

<template>
    <section class="py-16">
        <article class="container mx-auto px-4 lg:px-24 text-center">
            <h2 class="text-3xl md:text-5xl mb-4 modern-antiqua-regular">
                Upcoming Events
            </h2>
            <p class="text-lg modern-antiqua-regular">
                Check out our exciting upcoming events, from tournaments to game nights and expansion releases!
            </p>
            <div class="hidden md:block mt-8 pb-16 border-b-2 border-stone-500">
                <!-- Filters -->
                <div class="flex justify-center space-x-4">
                    <DefaultButton type="button" variant="outlined">
                        All Events
                    </DefaultButton>
                    <DefaultButton type="button" variant="outlined">
                        Tournaments
                    </DefaultButton>
                    <DefaultButton type="button" variant="outlined">
                        Game Nights
                    </DefaultButton>
                    <DefaultButton type="button" variant="outlined">
                        Expansion Releases
                    </DefaultButton>
                    <DefaultButton type="button" variant="outlined">
                        Special Events
                    </DefaultButton>
                </div>
            </div>
            <!-- Event Cards -->
            <div>
                <EventCard v-for="event in events" :key="event.title" :event="event" />
            </div>
        </article>
    </section>
</template>