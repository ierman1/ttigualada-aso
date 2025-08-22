<script setup lang="ts">
import { ref } from 'vue'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { faEnvelope, faPhone, faMapMarkerAlt } from '@fortawesome/free-solid-svg-icons';

const contactInfo = ref({
    email: 'contact@example.com',
    phone: '+1 (555) 123-4567',
    address: '123 Main St, Anytown, USA'
})
</script>

<template>
    <section class="py-16">
        <article class="container mx-auto px-4 lg:px-24 text-center modern-antiqua-regular">
            <h2 class="text-3xl md:text-5xl mb-4">
                Get in Touch
            </h2>
            <p class="text-lg">
                We would love to hear from you!
            </p>
            <div class="flex justify-between mt-12 space-x-8 flex-wrap md:flex-nowrap">
                <div class="flex flex-col items-center flex-1">
                    <FontAwesomeIcon class="text-4xl text-teal-500" :icon="faEnvelope" />
                    <div class="mt-4">
                        <h3 class="text-xl mb-2">Email</h3>
                        <p>Reach us anytime at our address below</p>
                        <p class="font-bold">{{ contactInfo.email }}</p>
                    </div>
                </div>
                <div class="flex flex-col items-center flex-1">
                    <FontAwesomeIcon class="text-4xl text-teal-500" :icon="faPhone" />
                    <div class="mt-4">
                        <h3 class="text-xl mb-2">Phone</h3>
                        <p>Call us at our number below</p>
                        <p class="font-bold">{{ contactInfo.phone }}</p>
                    </div>
                </div>
                <div class="flex flex-col items-center flex-1">
                    <FontAwesomeIcon class="text-4xl text-teal-500" :icon="faMapMarkerAlt" />
                    <div class="mt-4">
                        <h3 class="text-xl mb-2">Address</h3>
                        <p>Visit us at our office below</p>
                        <p class="font-bold">{{ contactInfo.address }}</p>
                    </div>
                </div>
            </div>
        </article>
    </section>
</template>