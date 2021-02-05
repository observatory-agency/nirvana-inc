<template>
    <section id="contact" class="relative bg-white">
        <div class="absolute inset-0">
            <div class="absolute inset-y-0 left-0 w-1/2 bg-gray-50"></div>
        </div>
        <div class="relative mx-auto max-w-7xl lg:grid lg:grid-cols-5">
            <div
                class="px-4 py-16 bg-gray-50 sm:px-6 lg:col-span-2 lg:px-8 lg:py-24 xl:pr-12"
            >
                <div class="max-w-lg mx-auto">
                    <h2
                        class="text-2xl font-extrabold tracking-tight text-gray-900 sm:text-3xl"
                    >
                        Contact us today for more information
                    </h2>
                    <dl class="mt-8 text-base text-gray-500">
                        <div class="mt-3">
                            <dt class="sr-only">Email</dt>
                            <dd class="flex">
                                <svg
                                    class="flex-shrink-0 w-6 h-6 text-gray-400"
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
                                        d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                                    />
                                </svg>
                                <span class="ml-3">
                                    pscreationd@gmail.com
                                </span>
                            </dd>
                        </div>
                    </dl>
                </div>
            </div>
            <div
                class="px-4 py-16 bg-white sm:px-6 lg:col-span-3 lg:py-24 lg:px-8 xl:pl-12"
            >
                <div class="max-w-lg mx-auto lg:max-w-none">
                    <form
                        name="contact-form"
                        method="POST"
                        netlify
                        netlify-honeypot="bot-field"
                        data-netlify-recaptcha="true"
                        class="grid grid-cols-1 gap-y-6"
                    >
                        <input
                            type="hidden"
                            name="form-name"
                            value="contact-form"
                        />
                        <div class="hidden">
                            <label for="bot-field"
                                >Don’t fill this out if you're human:</label
                            >
                            <input name="bot-field" />
                        </div>
                        <div>
                            <label for="full_name" class="sr-only"
                                >Full name</label
                            >
                            <input
                                type="text"
                                id="full_name"
                                name="full_name"
                                class="block w-full px-4 py-3 placeholder-gray-500 border-gray-300 rounded-md shadow-sm focus:ring-green-500 focus:border-green-500"
                                placeholder="Full name"
                                required
                            />
                        </div>
                        <div>
                            <label for="email" class="sr-only">Email</label>
                            <input
                                id="email"
                                type="email"
                                name="email"
                                class="block w-full px-4 py-3 placeholder-gray-500 border-gray-300 rounded-md shadow-sm focus:ring-green-500 focus:border-green-500"
                                placeholder="Email"
                                required
                            />
                        </div>
                        <div>
                            <label for="phone" class="sr-only">Phone</label>
                            <input
                                id="phone"
                                type="tel"
                                name="phone"
                                class="block w-full px-4 py-3 placeholder-gray-500 border-gray-300 rounded-md shadow-sm focus:ring-green-500 focus:border-green-500"
                                placeholder="Phone"
                                required
                            />
                        </div>
                        <div>
                            <label for="message" class="sr-only">Message</label>
                            <textarea
                                id="message"
                                name="message"
                                rows="4"
                                class="block w-full px-4 py-3 placeholder-gray-500 border-gray-300 rounded-md shadow-sm focus:ring-green-500 focus:border-green-500"
                                placeholder="Message"
                                required
                            ></textarea>
                        </div>
                        <div>
                            <div
                                data-netlify-recaptcha="true"
                                class="field"
                            ></div>
                            <button
                                type="submit"
                                class="inline-flex justify-center px-6 py-3 mt-4 text-base font-medium text-white bg-green-600 border border-transparent rounded-md shadow-sm hover:bg-green-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-green-500"
                            >
                                Submit
                            </button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {}
</script>
