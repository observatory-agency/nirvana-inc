<template>
    <section id="faq" class="py-12 content-wrapper lg:py-24">
        <div class="grid gap-8 lg:grid-cols-2">
            <div>
                <h3
                    class="text-2xl font-extrabold tracking-tight text-gray-900 sm:text-3xl"
                >
                    FAQ
                </h3>
                <p class="my-4">
                    Our Program treats patients with dependencies to the
                    following substances:
                </p>
                <div class="flex flex-col lg:flex-row lg:space-x-10">
                    <ul>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Alcohol
                        </li>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Amphetamines
                        </li>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Benzodiazepines
                        </li>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Cocaine
                        </li>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Cigarettes
                        </li>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Gambling
                        </li>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Over Eating
                        </li>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Marijuana
                        </li>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Opioids
                        </li>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Sugar
                        </li>
                    </ul>
                    <ul>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Depression
                        </li>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Anxiety
                        </li>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Bipolar
                        </li>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Schizophrenia
                        </li>
                        <li class="text-lg text-gray-700 list-disc list-inside">
                            Autoimmune disorders
                        </li>
                    </ul>
                </div>
                <div class="relative hidden lg:block">
                    <LeafOne />
                    <LeafTwo class="z-50 lg:absolute left-64 bottom-24" />
                    <LeafThree />
                </div>
            </div>
            <div>
                <div></div>
                <div>
                    <img src="~/assets/img/medical-tree.png" alt="" />
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {}
</script>
