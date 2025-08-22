<script setup lang="ts">
import { ref } from 'vue'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { faTwitter, faInstagram, faTiktok } from '@fortawesome/free-brands-svg-icons';

const socialLinks = ref([
    { name: 'Twitter', url: 'https://twitter.com', icon: faTwitter },
    { name: 'Instagram', url: 'https://instagram.com', icon: faInstagram },
    { name: 'TikTok', url: 'https://tiktok.com', icon: faTiktok }
])
</script>

<template>
    <section class="py-16">
        <article class="container mx-auto px-4 lg:px-24 text-center modern-antiqua-regular">
            <h2 class="text-3xl md:text-5xl mb-4">
                Follow Us
            </h2>
            <p class="text-lg">
                Stay connected with us on social media.
            </p>
            <div class="flex justify-center space-x-4 mt-8">
                <a 
                    v-for="social in socialLinks"
                    :key="social.name"
                    :href="social.url"
                    class="text-teal-500 text-4xl"
                >
                    <FontAwesomeIcon :icon="social.icon" />
                </a>
            </div>
        </article>
    </section>
</template>