<script setup lang="ts">
import DefaultButton from '../components/DefaultButton.vue';

</script>

<template>
    <section class="py-16 mt-10">
        <article class="container mx-auto px-4 flex flex-col lg:flex-row items-baseline lg:gap-8">
            <h1 class="text-4xl md:text-6xl mb-4 modern-antiqua-regular">Welcome to your tabletop gaming haven!</h1>
            <div>
                <p class="text-lg modern-antiqua-regular">Join us for an exciting adventure in tabletop gaming! From Magic: The Gathering to Dungeons & Dragons, we provide a welcoming space for players of all levels.</p>
                <DefaultButton type="link" href="/reserve" class="mt-4">
                    Reserve a table
                </DefaultButton>
            </div>
        </article>
        <article class="container mx-auto px-4">
            <img src="/src/assets/mtg_banner_1.jpg" alt="Welcome Image" class="w-full h-auto mt-8 rounded-lg shadow-lg">
            <p class="text-sm mt-1">
                "<a rel="noopener noreferrer" href="https://commons.wikimedia.org/w/index.php?curid=43348832">Magic the Gathering - Commander</a>" by <a rel="noopener noreferrer" href="https://commons.wikimedia.org/w/index.php?title=User:Tourtefouille&action=edit&redlink=1">Tourtefouille</a> is licensed under <a rel="noopener noreferrer" href="https://creativecommons.org/licenses/by-sa/4.0/?ref=openverse">CC BY-SA 4.0 <img src="https://mirrors.creativecommons.org/presskit/icons/cc.svg" style="height: 1em; margin-right: 0.125em; display: inline;" /><img src="https://mirrors.creativecommons.org/presskit/icons/by.svg" style="height: 1em; margin-right: 0.125em; display: inline;" /><img src="https://mirrors.creativecommons.org/presskit/icons/sa.svg" style="height: 1em; margin-right: 0.125em; display: inline;" /></a>.
            </p>
        </article>
    </section>
</template>