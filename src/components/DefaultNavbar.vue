<script setup lang="ts">
import { ref } from 'vue'

const isMobileMenuOpen = ref(false)
const isMoreInfoOpen = ref(false)

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const toggleMoreInfo = () => {
  isMoreInfoOpen.value = !isMoreInfoOpen.value
}

const closeMobileMenu = () => {
  isMobileMenuOpen.value = false
}

const closeMoreInfo = () => {
  isMoreInfoOpen.value = false
}
</script>

<template>
    <nav class="px-4 py-2 bg-gray-100 text-stone-900 dark:bg-stone-900 dark:text-gray-100 shadow-md relative">
        <div class="flex items-center">

            <!-- Logo - Left Side -->
            <div class="flex items-center">
                <img src="/src/assets/logo.png" alt="Logo" class="h-10 w-10">
            </div>

            <!-- Desktop Navigation - Centered -->
            <div class="flex-1 flex justify-center">
                <ul class="hidden md:flex space-x-6 modern-antiqua-regular text-xl">
                <li>
                    <a href="/" class="hover:text-gray-600 dark:hover:text-gray-400 transition-colors">Home Page</a>
                </li>
                <li>
                    <a href="/events" class="hover:text-gray-600 dark:hover:text-gray-400 transition-colors">Events List</a>
                </li>
                <li>
                    <a href="/reserve" class="hover:text-gray-600 dark:hover:text-gray-400 transition-colors">Reserve Table</a>
                </li>
                <li class="relative">
                    <button 
                        @click="toggleMoreInfo"
                        @blur="closeMoreInfo"
                        class="hover:text-gray-600 dark:hover:text-gray-400 transition-colors flex items-center"
                    >
                        More Info
                        <svg class="ml-1 w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                            <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
                        </svg>
                    </button>

                    <!-- Desktop More Info Dropdown -->
                    <div 
                        v-show="isMoreInfoOpen"
                        class="absolute right-0 mt-2 w-48 bg-gray-100 text-stone-900 dark:bg-stone-900 dark:text-gray-100 rounded-md shadow-lg z-50 border border-gray-300 dark:border-gray-600"
                    >
                        <div class="py-1">
                            <a href="/contact" class="block px-4 py-2 text-sm hover:bg-gray-200 dark:hover:bg-gray-700 transition-colors">Contact Us</a>
                            <a href="/privacy" class="block px-4 py-2 text-sm hover:bg-gray-200 dark:hover:bg-gray-700 transition-colors">Privacy Policy</a>
                            <a href="/terms" class="block px-4 py-2 text-sm hover:bg-gray-200 dark:hover:bg-gray-700 transition-colors">Terms of Service</a>
                        </div>
                    </div>
                </li>
            </ul>
            </div>

            <!-- Mobile Hamburger Button -->
            <button 
                @click="toggleMobileMenu"
                class="md:hidden flex items-center justify-center w-8 h-8 hover:bg-gray-200 dark:hover:bg-gray-700 rounded transition-colors"
            >
                <svg 
                    class="w-6 h-6" 
                    fill="none" 
                    stroke="currentColor" 
                    viewBox="0 0 24 24"
                >
                    <path 
                        v-if="!isMobileMenuOpen"
                        stroke-linecap="round" 
                        stroke-linejoin="round" 
                        stroke-width="2" 
                        d="M4 6h16M4 12h16M4 18h16"
                    />
                    <path 
                        v-else
                        stroke-linecap="round" 
                        stroke-linejoin="round" 
                        stroke-width="2" 
                        d="M6 18L18 6M6 6l12 12"
                    />
                </svg>
            </button>
        </div>

        <!-- Mobile Menu Dropdown -->
        <div 
            v-show="isMobileMenuOpen"
            class="md:hidden absolute top-full left-0 right-0 bg-gray-100 text-stone-900 dark:bg-stone-900 dark:text-gray-100 border-t border-gray-300 dark:border-gray-600 shadow-lg z-50"
        >
            <div class="py-2">
                <a 
                    href="/" 
                    @click="closeMobileMenu"
                    class="block px-4 py-3 modern-antiqua-regular text-lg hover:bg-gray-200 dark:hover:bg-gray-700 transition-colors"
                >
                    Home Page
                </a>
                <a 
                    href="/events" 
                    @click="closeMobileMenu"
                    class="block px-4 py-3 modern-antiqua-regular text-lg hover:bg-gray-200 dark:hover:bg-gray-700 transition-colors"
                >
                    Events List
                </a>
                <a 
                    href="/reserve" 
                    @click="closeMobileMenu"
                    class="block px-4 py-3 modern-antiqua-regular text-lg hover:bg-gray-200 dark:hover:bg-gray-700 transition-colors"
                >
                    Reserve Table
                </a>
                <a 
                    href="/contact" 
                    @click="closeMobileMenu"
                    class="block px-4 py-3 modern-antiqua-regular text-lg hover:bg-gray-200 dark:hover:bg-gray-700 transition-colors"
                >
                    Contact Us
                </a>
                <a 
                    href="/privacy" 
                    @click="closeMobileMenu"
                    class="block px-4 py-3 modern-antiqua-regular text-lg hover:bg-gray-200 dark:hover:bg-gray-700 transition-colors"
                >
                    Privacy Policy
                </a>
                <a 
                    href="/terms" 
                    @click="closeMobileMenu"
                    class="block px-4 py-3 modern-antiqua-regular text-lg hover:bg-gray-200 dark:hover:bg-gray-700 transition-colors"
                >
                    Terms of Service
                </a>
            </div>
        </div>
    </nav>
</template>