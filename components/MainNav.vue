<template>
    <div class="relative bg-white">
        <div class="relative z-20 shadow">
            <div
                class="flex items-center justify-between px-4 py-5 mx-auto max-w-7xl sm:px-6 sm:py-4 lg:px-8"
            >
                <div>
                    <h1>Nirvana, Inc</h1>
                </div>
                <div class="-my-2 -mr-2 md:hidden">
                    <button
                        type="button"
                        class="inline-flex items-center justify-center p-2 text-gray-400 bg-white rounded-md hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-green-500"
                        @click="mobileMenu = !mobileMenu"
                    >
                        <span class="sr-only">Open menu</span>
                        <!-- Heroicon name: menu -->
                        <svg
                            class="w-6 h-6"
                            xmlns="http://www.w3.org/2000/svg"
                            fill="none"
                            viewBox="0 0 24 24"
                            stroke="currentColor"
                            aria-hidden="true"
                        >
                            <path
                                stroke-linecap="round"
                                stroke-linejoin="round"
                                stroke-width="2"
                                d="M4 6h16M4 12h16M4 18h16"
                            />
                        </svg>
                    </button>
                </div>
                <div class="hidden md:flex md:items-center md:justify-between">
                    <nav class="flex space-x-8">
                        <nuxt-link
                            v-for="item in mainNav"
                            :key="item.anchor"
                            :to="item.anchor"
                            class="text-base font-medium text-gray-500 hover:text-gray-900"
                        >
                            {{ item.title }}
                        </nuxt-link>
                    </nav>
                </div>
            </div>
        </div>

        <transition
            enter-active-class="transition duration-200 ease-out"
            enter-class="translate-y-1 opacity-0"
            enter-to-class="translate-y-0 opacity-100"
            leave-active-class="transition duration-150 ease-in"
            leave-class="translate-y-0 opacity-100"
            leave-to-class="translate-y-1 opacity-0"
        >
            <div
                v-show="mobileMenu"
                class="absolute inset-x-0 top-0 z-30 p-2 transition origin-top-right transform md:hidden"
            >
                <div
                    class="bg-white divide-y-2 rounded-lg shadow-lg ring-1 ring-black ring-opacity-5 divide-gray-50"
                >
                    <div class="px-5 pt-5 pb-6 sm:pb-8">
                        <div class="flex items-center justify-between">
                            <div>
                                <h1>Nirvana Inc</h1>
                            </div>
                            <div class="-mr-2">
                                <button
                                    type="button"
                                    class="inline-flex items-center justify-center p-2 text-gray-400 bg-white rounded-md hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-green-500"
                                    @click="mobileMenu = false"
                                >
                                    <span class="sr-only">Close menu</span>
                                    <!-- Heroicon name: x -->
                                    <svg
                                        class="w-6 h-6"
                                        xmlns="http://www.w3.org/2000/svg"
                                        fill="none"
                                        viewBox="0 0 24 24"
                                        stroke="currentColor"
                                        aria-hidden="true"
                                    >
                                        <path
                                            stroke-linecap="round"
                                            stroke-linejoin="round"
                                            stroke-width="2"
                                            d="M6 18L18 6M6 6l12 12"
                                        />
                                    </svg>
                                </button>
                            </div>
                        </div>
                    </div>
                    <div class="px-5 py-6">
                        <nav class="grid grid-cols-2 gap-4">
                            <nuxt-link
                                v-for="item in mainNav"
                                :key="item.anchor"
                                :to="item.anchor"
                                class="text-base font-medium text-gray-500 hover:text-gray-900"
                            >
                                {{ item.title }}
                            </nuxt-link>
                        </nav>
                    </div>
                </div>
            </div>
        </transition>
    </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
    data() {
        return {
            mobileMenu: false,
        }
    },
    computed: {
        ...mapState(['mainNav']),
    },
}
</script>
