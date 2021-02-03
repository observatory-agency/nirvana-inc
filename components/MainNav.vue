<template>
    <!-- This example requires Tailwind CSS v2.0+ -->
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

        <!--
    Mobile menu, show/hide based on mobile menu state.

    Entering: "duration-200 ease-out"
      From: "opacity-0 scale-95"
      To: "opacity-100 scale-100"
    Leaving: "duration-100 ease-in"
      From: "opacity-100 scale-100"
      To: "opacity-0 scale-95"
  -->
        <div
            class="absolute inset-x-0 top-0 z-30 p-2 transition origin-top-right transform md:hidden"
        >
            <div
                class="bg-white divide-y-2 rounded-lg shadow-lg ring-1 ring-black ring-opacity-5 divide-gray-50"
            >
                <div class="px-5 pt-5 pb-6 sm:pb-8">
                    <div class="flex items-center justify-between">
                        <div>
                            <img
                                class="w-auto h-8"
                                src="https://tailwindui.com/img/logos/workflow-mark-green-600.svg"
                                alt="Workflow"
                            />
                        </div>
                        <div class="-mr-2">
                            <button
                                type="button"
                                class="inline-flex items-center justify-center p-2 text-gray-400 bg-white rounded-md hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-green-500"
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
                    <div class="mt-6 sm:mt-8">
                        <nav>
                            <div
                                class="grid gap-7 sm:grid-cols-2 sm:gap-y-8 sm:gap-x-4"
                            >
                                <a
                                    href="#"
                                    class="flex items-center p-3 -m-3 rounded-lg hover:bg-gray-50"
                                >
                                    <div
                                        class="flex items-center justify-center flex-shrink-0 w-10 h-10 text-white bg-green-500 rounded-md sm:h-12 sm:w-12"
                                    >
                                        <!-- Heroicon name: chart-bar -->
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
                                                d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"
                                            />
                                        </svg>
                                    </div>
                                    <div
                                        class="ml-4 text-base font-medium text-gray-900"
                                    >
                                        Analytics
                                    </div>
                                </a>

                                <a
                                    href="#"
                                    class="flex items-center p-3 -m-3 rounded-lg hover:bg-gray-50"
                                >
                                    <div
                                        class="flex items-center justify-center flex-shrink-0 w-10 h-10 text-white bg-green-500 rounded-md sm:h-12 sm:w-12"
                                    >
                                        <!-- Heroicon name: cursor-click -->
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
                                                d="M15 15l-2 5L9 9l11 4-5 2zm0 0l5 5M7.188 2.239l.777 2.897M5.136 7.965l-2.898-.777M13.95 4.05l-2.122 2.122m-5.657 5.656l-2.12 2.122"
                                            />
                                        </svg>
                                    </div>
                                    <div
                                        class="ml-4 text-base font-medium text-gray-900"
                                    >
                                        Engagement
                                    </div>
                                </a>

                                <a
                                    href="#"
                                    class="flex items-center p-3 -m-3 rounded-lg hover:bg-gray-50"
                                >
                                    <div
                                        class="flex items-center justify-center flex-shrink-0 w-10 h-10 text-white bg-green-500 rounded-md sm:h-12 sm:w-12"
                                    >
                                        <!-- Heroicon name: shield-check -->
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
                                                d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"
                                            />
                                        </svg>
                                    </div>
                                    <div
                                        class="ml-4 text-base font-medium text-gray-900"
                                    >
                                        Security
                                    </div>
                                </a>

                                <a
                                    href="#"
                                    class="flex items-center p-3 -m-3 rounded-lg hover:bg-gray-50"
                                >
                                    <div
                                        class="flex items-center justify-center flex-shrink-0 w-10 h-10 text-white bg-green-500 rounded-md sm:h-12 sm:w-12"
                                    >
                                        <!-- Heroicon name: view-grid -->
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
                                                d="M4 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2V6zM14 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V6zM4 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2v-2zM14 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z"
                                            />
                                        </svg>
                                    </div>
                                    <div
                                        class="ml-4 text-base font-medium text-gray-900"
                                    >
                                        Integrations
                                    </div>
                                </a>
                            </div>
                            <div class="mt-8 text-base">
                                <a
                                    href="#"
                                    class="font-medium text-green-600 hover:text-green-500"
                                >
                                    View all products
                                    <span aria-hidden="true">&rarr;</span></a
                                >
                            </div>
                        </nav>
                    </div>
                </div>
                <div class="px-5 py-6">
                    <div class="grid grid-cols-2 gap-4">
                        <a
                            href="#"
                            class="text-base font-medium text-gray-900 rounded-md hover:text-gray-700"
                        >
                            Pricing
                        </a>

                        <a
                            href="#"
                            class="text-base font-medium text-gray-900 rounded-md hover:text-gray-700"
                        >
                            Docs
                        </a>

                        <a
                            href="#"
                            class="text-base font-medium text-gray-900 rounded-md hover:text-gray-700"
                        >
                            Company
                        </a>

                        <a
                            href="#"
                            class="text-base font-medium text-gray-900 rounded-md hover:text-gray-700"
                        >
                            Resources
                        </a>

                        <a
                            href="#"
                            class="text-base font-medium text-gray-900 rounded-md hover:text-gray-700"
                        >
                            Blog
                        </a>

                        <a
                            href="#"
                            class="text-base font-medium text-gray-900 rounded-md hover:text-gray-700"
                        >
                            Contact Sales
                        </a>
                    </div>
                    <div class="mt-6">
                        <a
                            href="#"
                            class="flex items-center justify-center w-full px-4 py-2 text-base font-medium text-white bg-green-600 border border-transparent rounded-md shadow-sm hover:bg-green-700"
                        >
                            Sign up
                        </a>
                        <p
                            class="mt-6 text-base font-medium text-center text-gray-500"
                        >
                            Existing customer?
                            <a
                                href="#"
                                class="text-green-600 hover:text-green-500"
                            >
                                Sign in
                            </a>
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
    computed: {
        ...mapState(['mainNav']),
    },
}
</script>

<style lang="scss" scoped></style>
