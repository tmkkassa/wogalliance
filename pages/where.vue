<template>
    <div>
        <Navbar :navlight="true" />

        <!-- Hero Section -->
        <section class="relative table w-full py-32 lg:py-44 bg-no-repeat bg-center bg-cover"
            :style="{ backgroundImage: `url(${bg})` }">
            <div class="absolute inset-0 bg-black opacity-80"></div>
            <div class="container relative">
                <div class="grid grid-cols-1 text-center mt-10">
                    <h3 class="md:text-3xl text-2xl md:leading-normal leading-normal font-semibold text-white">Where We
                        Work</h3>
                    <p class="text-white mt-4 max-w-2xl mx-auto">Discover our reach and impact across Wolayta,
                        Ethiopia and the DMV area</p>
                </div>
            </div>
        </section>

        <!-- Shape Divider -->
        <div class="relative">
            <div class="shape overflow-hidden z-1 text-white dark:text-slate-900">
                <svg viewBox="0 0 2880 48" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M0 48H1437.5H2880V0H2160C1442.5 52 720 0 720 0H0V48Z" fill="currentColor"></path>
                </svg>
            </div>
        </div>

        <!-- Main Content Section -->
        <section class="relative lg:py-24 py-16">
            <div class="container relative">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-center">
                    <!-- Content -->
                    <div class="lg:order-1 order-2">
                        <div class="lg:me-5 m-2">
                            <h4 class="mb-6 md:text-3xl text-2xl md:leading-normal leading-normal font-semibold">Our
                                Global Reach</h4>
                            <p class="text-slate-400 mb-6 leading-relaxed">
                                We are registered with a license from Government of the District of Colombia, Washington
                                DC. We initiate serving our member Wolayta immigrants concentrated in the DMV area and
                                extending the function to Wolayta immigrants outside the DMV area in USA and beyond
                                through a special membership framework of associateship and networking.
                            </p>
                            <p class="text-slate-400 mb-6 leading-relaxed">
                                We engage in sociocultural, civic, human rights and humanitarian affairs affecting our
                                community of origin in Ethiopia.
                            </p>

                            <!-- Key Points -->
                            <div class="grid grid-cols-1 gap-4 mt-8">
                                <div class="flex items-start space-x-3">
                                    <div
                                        class="flex-shrink-0 w-6 h-6  rounded-full flex items-center justify-center mt-1">
                                        <i class="iconoir-check-circle text-primary text-sm"></i>
                                    </div>
                                    <div>
                                        <h6 class="font-semibold text-slate-900 dark:text-white">Government Licensed
                                        </h6>
                                        <p class="text-slate-400 text-sm">Registered with District of Colombia,
                                            Washington DC</p>
                                    </div>
                                </div>

                                <div class="flex items-start space-x-3">
                                    <div
                                        class="flex-shrink-0 w-6 h-6 rounded-full flex items-center justify-center mt-1">
                                        <i class="iconoir-check-circle text-primary text-sm"></i>
                                    </div>
                                    <div>
                                        <h6 class="font-semibold text-slate-900 dark:text-white">DMV Focus</h6>
                                        <p class="text-slate-400 text-sm">Serving Wolayta immigrants in the DMV area</p>
                                    </div>
                                </div>

                                <div class="flex items-start space-x-3">
                                    <div
                                        class="flex-shrink-0 w-6 h-6 rounded-full flex items-center justify-center mt-1">
                                        <i class="iconoir-check-circle text-primary text-sm"></i>
                                    </div>
                                    <div>
                                        <h6 class="font-semibold text-slate-900 dark:text-white">Global Network</h6>
                                        <p class="text-slate-400 text-sm">Extending services beyond DMV across USA and
                                            worldwide</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Image/Visual -->
                    <div class="lg:order-2 order-1">
                        <div class="relative">
                            <div class="bg-gradient-to-br from-primary/10 to-primary/5 rounded-2xl p-8">
                                <div class="text-center">
                                    <div
                                        class="size-20 bg-primary/10 text-primary rounded-2xl flex align-middle justify-center items-center shadow-sm mx-auto mb-4">
                                        <i class="iconoir-globe text-4xl"></i>
                                    </div>
                                    <h5 class="text-xl font-semibold mb-2">Wolayta Community</h5>
                                    <p class="text-slate-400">Connecting communities across continents</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Maps Section -->
        <section class="relative lg:py-24 py-16 bg-slate-50 dark:bg-slate-800/50">
            <div class="container relative">
                <div class="grid grid-cols-1 pb-6 text-center">
                    <h4 class="mb-6 md:text-3xl text-2xl md:leading-normal leading-normal font-semibold">Our Geographic
                        Presence</h4>
                    <p class="text-slate-400 max-w-xl mx-auto">Explore our reach from the heart of Wolayta, Ethiopia to
                        the vibrant DMV metropolitan area</p>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-2 mt-12">
                    <!-- Wolayta, Ethiopia Map -->
                    <div class="flex">
                        <div
                            class="bg-white dark:bg-slate-900 rounded-xl shadow-lg dark:shadow-gray-700 overflow-hidden w-full m-2">
                            <div class="p-6 border-b border-slate-100 dark:border-slate-800">
                                <h5 class="text-xl font-semibold mb-2 flex items-center">
                                    <i class="iconoir-map-pin text-primary mr-2"></i>
                                    Wolayta, Ethiopia
                                </h5>
                                <p class="text-slate-400 text-sm">Our community of origin</p>
                            </div>
                            <div class="p-0">
                                <iframe
                                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3940.5!2d37.7!3d7.0!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zN8KwMDAnMDAuMCJOIDM3wrA0MicwMC4wIkU!5e0!3m2!1sen!2sus!4v1234567890!5m2!1sen!2sus"
                                    style="border:0" class="w-full h-80" allowfullscreen>
                                </iframe>
                            </div>
                            <div class="p-6 bg-slate-50 dark:bg-slate-800">
                                <div class="flex items-center justify-between">
                                    <div>
                                        <h6 class="font-semibold text-slate-900 dark:text-white">Wolayta Zone</h6>
                                        <p class="text-slate-400 text-sm">Southern Nations, Nationalities, and Peoples'
                                            Region</p>
                                    </div>
                                    <div class="text-right">
                                        <span
                                            class="inline-flex items-center px-3 py-1 rounded-full text-xs font-medium bg-violet-100 text-violet-800 dark:bg-violet-900 dark:text-violet-200">
                                            Ethiopia
                                        </span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>


                    <!-- DMV Area Map -->
                    <div class="flex">
                        <div
                            class="bg-white dark:bg-slate-900 rounded-xl shadow-lg dark:shadow-gray-700 overflow-hidden w-full m-2">
                            <div class="p-6 border-b border-slate-100 dark:border-slate-800">
                                <h5 class="text-xl font-semibold mb-2 flex items-center">
                                    <i class="iconoir-map-pin text-primary mr-2"></i>
                                    DMV Metropolitan Area
                                </h5>
                                <p class="text-slate-400 text-sm">Washington DC, Maryland, Virginia</p>
                            </div>
                            <div class="p-0">
                                <iframe
                                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d19866.5!2d-77.0!3d38.9!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89b7c6de5af6e45b%3A0xc242012f3de0a41d!2sWashington%2C%20DC%2C%20USA!5e0!3m2!1sen!2sus!4v1234567890!5m2!1sen!2sus"
                                    style="border:0" class="w-full h-80" allowfullscreen>
                                </iframe>
                            </div>
                            <div class="p-6 bg-slate-50 dark:bg-slate-800">
                                <div class="flex items-center justify-between">
                                    <div>
                                        <h6 class="font-semibold text-slate-900 dark:text-white">Capital Region</h6>
                                        <p class="text-slate-400 text-sm">District of Columbia, Maryland, Virginia</p>
                                    </div>
                                    <div class="text-right">
                                        <span
                                            class="inline-flex items-center px-3 py-1 rounded-full text-xs font-medium bg-green-100 text-green-800 dark:bg-green-900 dark:text-green-200">
                                            USA
                                        </span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>


                <!-- Additional Info -->
                <div class="grid grid-cols-1 lg:grid-cols-3 gap-6 mt-16">
                    <div class="text-center px-6">
                        <div
                            class="size-16 bg-primary/5 text-primary rounded-2xl flex align-middle justify-center items-center shadow-sm mx-auto">
                            <i class="iconoir-community text-3xl"></i>
                        </div>
                        <div class="content mt-4">
                            <h5 class="text-lg font-semibold">Community Focus</h5>
                            <p class="text-slate-400 mt-3">Serving Wolayta immigrants and their families across the
                                region</p>
                        </div>
                    </div>

                    <div class="text-center px-6">
                        <div
                            class="size-16 bg-primary/5 text-primary rounded-2xl flex align-middle justify-center items-center shadow-sm mx-auto">
                            <i class="iconoir-user-love text-3xl"></i>
                        </div>
                        <div class="content mt-4">
                            <h5 class="text-lg font-semibold">Humanitarian Aid</h5>
                            <p class="text-slate-400 mt-3">Supporting our community of origin in Ethiopia</p>
                        </div>
                    </div>

                    <div class="text-center px-6">
                        <div
                            class="size-16 bg-primary/5 text-primary rounded-2xl flex align-middle justify-center items-center shadow-sm mx-auto">
                            <i class="iconoir-network text-3xl"></i>
                        </div>
                        <div class="content mt-4">
                            <h5 class="text-lg font-semibold">Global Network</h5>
                            <p class="text-slate-400 mt-3">Building connections across continents and cultures</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <Footer />

        <Switcher />

        <ScrollToTop />

    </div>
</template>

<script setup>
import bg from '@/assets/images/gifata3.jpeg'
</script>
