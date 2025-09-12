<template>
    <div>
        <Navbar :navlight="true" />

        <!-- Hero Section -->
        <section class="relative table w-full py-32 lg:py-44 bg-no-repeat bg-center bg-cover"
            :style="{ backgroundImage: `url(${bg})` }">
            <div class="absolute inset-0 bg-black opacity-80"></div>
            <div class="container relative">
                <div class="grid grid-cols-1 text-center mt-10">
                    <h3 class="md:text-4xl text-3xl md:leading-normal leading-normal font-bold text-white mb-4">Get
                        Involved</h3>
                    <p class="text-lg text-gray-200 max-w-3xl mx-auto">We believe in alliance, association and
                        networking for self-help and helping others. Join us in making a difference.</p>
                </div>
            </div>
        </section>

        <div class="relative">
            <div class="shape overflow-hidden z-1 text-white dark:text-slate-900">
                <svg viewBox="0 0 2880 48" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M0 48H1437.5H2880V0H2160C1442.5 52 720 0 720 0H0V48Z" fill="currentColor"></path>
                </svg>
            </div>
        </div>

        <!-- Mission Statement Section -->
        <section class="relative lg:py-24 py-16 bg-gray-50 dark:bg-slate-900">
            <div class="container relative">
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <div class="lg:order-2">
                        <div class="relative">
                            <div class="relative z-10">
                                <img :src="bg" class="rounded-lg shadow-2xl" alt="Community Involvement">
                            </div>
                            <div
                                class="absolute -bottom-6 -left-6 w-24 h-24 bg-gradient-to-r from-primary to-blue-400 rounded-full opacity-20">
                            </div>
                            <div
                                class="absolute -top-6 -right-6 w-32 h-32 bg-gradient-to-r from-blue-400 to-primary rounded-full opacity-20">
                            </div>
                        </div>
                    </div>

                    <div class="lg:order-1">
                        <div class="flex items-center mb-6">
                            <div
                                class="w-12 h-12 bg-gradient-to-r from-primary to-blue-400 rounded-lg flex items-center justify-center mr-4 shadow-lg">
                                <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                        d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z">
                                    </path>
                                </svg>
                            </div>
                            <h2 class="text-3xl font-bold text-gray-900 dark:text-white">Our Mission</h2>
                        </div>
                        <p class="text-lg text-gray-600 dark:text-gray-300 leading-relaxed mb-6">
                            We know immigrants' integration, community empowerment, successfully implementing
                            humanitarian actions
                            and promoting human rights demand social, practical and material provisions. We welcome your
                            involvement
                            in support of our work.
                        </p>
                        <p class="text-lg text-gray-600 dark:text-gray-300 leading-relaxed">
                            Every contribution, whether big or small, helps us create positive change in communities
                            worldwide.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Involvement Options Section -->
        <section class="relative lg:py-24 py-16">
            <div class="container relative">
                <div class="grid grid-cols-1 text-center">
                    <h3 class="mb-6 md:text-3xl text-2xl md:leading-normal leading-normal font-semibold">How You Can Get
                        Involved</h3>
                    <p class="text-slate-400 max-w-xl mx-auto">Choose the way that best fits your passion and
                        availability to make a meaningful impact.</p>
                </div>

                <div class="grid md:grid-cols-3 gap-6 mt-16">
                    <!-- Join Us Card -->
                    <div
                        class="group p-6 rounded-xl bg-white dark:bg-slate-800 border border-gray-200 dark:border-slate-700 hover:shadow-lg transition-all duration-300 hover:-translate-y-2">
                        <div
                            class="w-14 h-14 bg-gradient-to-r from-primary to-blue-400 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300 shadow-md">
                            <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-3">Join Us</h3>
                        <p class="text-gray-600 dark:text-gray-300">
                            Become part of our community and help us create positive change. Every member brings unique
                            skills and perspectives.
                        </p>
                        <div class="mt-4">
                            <a href="/contactus"
                                class="btn btn-link text-primary hover:text-primary after:bg-primary transition duration-500">
                                Become a Member
                            </a>
                        </div>
                    </div>

                    <!-- Donate Card -->
                    <div
                        class="group p-6 rounded-xl bg-white dark:bg-slate-800 border border-gray-200 dark:border-slate-700 hover:shadow-lg transition-all duration-300 hover:-translate-y-2">
                        <div
                            class="w-14 h-14 bg-gradient-to-r from-blue-400 to-primary rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300 shadow-md">
                            <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-3">Donate</h3>
                        <p class="text-gray-600 dark:text-gray-300">
                            Your financial support helps us continue our humanitarian work and expand our reach to more
                            communities in need.
                        </p>
                        <div class="mt-4">
                            <a href="/contactus"
                                class="btn btn-link text-blue-400 hover:text-blue-400 after:bg-blue-400 transition duration-500">
                                Make a Donation
                            </a>
                        </div>
                    </div>

                    <!-- Learn More Card -->
                    <div
                        class="group p-6 rounded-xl bg-white dark:bg-slate-800 border border-gray-200 dark:border-slate-700 hover:shadow-lg transition-all duration-300 hover:-translate-y-2">
                        <div
                            class="w-14 h-14 bg-gradient-to-r from-primary to-blue-400 rounded-lg flex items-center justify-center mb-4 group-hover:scale-110 transition-transform duration-300 shadow-md">
                            <svg class="w-7 h-7 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.746 0 3.332.477 4.5 1.253v13C19.832 18.477 18.246 18 16.5 18c-1.746 0-3.332.477-4.5 1.253">
                                </path>
                            </svg>
                        </div>
                        <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-3">Learn More</h3>
                        <p class="text-gray-600 dark:text-gray-300">
                            Discover how you can get involved and make a meaningful impact. Explore our programs and
                            initiatives.
                        </p>
                        <div class="mt-4">
                            <a href="/aboutus"
                                class="btn btn-link text-primary hover:text-primary after:bg-primary transition duration-500">
                                Explore Programs
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Call to Action Section -->
        <section class="relative lg:py-24 py-16">
            <div class="container relative">
                <div
                    class="bg-gradient-to-r from-primary to-blue-600 rounded-3xl p-12 text-center text-white shadow-2xl">
                    <div class="max-w-4xl mx-auto">
                        <h2 class="text-4xl font-bold mb-6">Ready to Make a Difference?</h2>
                        <p class="text-xl text-blue-100 mb-8 leading-relaxed">
                            Learn more about how you can get involved and contribute to our mission of
                            community empowerment and human rights advocacy.
                        </p>
                        <div class="flex flex-col sm:flex-row gap-4 justify-center">
                            <a href="/contactus"
                                class="inline-flex items-center px-8 py-4 bg-white text-primary font-semibold rounded-lg hover:bg-gray-100 transition-colors duration-300 shadow-lg">
                                <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                        d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z">
                                    </path>
                                </svg>
                                Contact Us Today
                            </a>
                            <a href="/aboutus"
                                class="inline-flex items-center px-8 py-4 bg-transparent border-2 border-white text-white font-semibold rounded-lg hover:bg-white hover:text-primary transition-all duration-300 shadow-lg">
                                <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                        d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.746 0 3.332.477 4.5 1.253v13C19.832 18.477 18.246 18 16.5 18c-1.746 0-3.332.477-4.5 1.253">
                                    </path>
                                </svg>
                                Learn More About Us
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Stats Section -->
        <section class="relative lg:py-24 py-16 bg-gray-50 dark:bg-slate-900">
            <div class="container relative">
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                    <div class="text-center">
                        <div class="text-4xl font-bold text-primary mb-2">500+</div>
                        <div class="text-gray-600 dark:text-gray-300">Active Volunteers</div>
                    </div>
                    <div class="text-center">
                        <div class="text-4xl font-bold text-blue-400 mb-2">$50K+</div>
                        <div class="text-gray-600 dark:text-gray-300">Funds Raised</div>
                    </div>
                    <div class="text-center">
                        <div class="text-4xl font-bold text-primary mb-2">25+</div>
                        <div class="text-gray-600 dark:text-gray-300">Programs Launched</div>
                    </div>
                    <div class="text-center">
                        <div class="text-4xl font-bold text-blue-400 mb-2">1000+</div>
                        <div class="text-gray-600 dark:text-gray-300">Lives Impacted</div>
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
import bg from '@/assets/images/bg/2.jpg'

definePageMeta({
    title: 'Get Involved - Join Our Mission',
    description: 'Learn how you can get involved in our mission of community empowerment, immigrant integration, and human rights advocacy. Join us, donate, or learn more about our programs.'
})

useHead({
    title: 'Get Involved - Join Our Mission',
    meta: [
        { name: 'description', content: 'Learn how you can get involved in our mission of community empowerment, immigrant integration, and human rights advocacy. Join us, donate, or learn more about our programs.' }
    ]
})
</script>

<style scoped>
/* Custom animations */
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.animate-fade-in-up {
    animation: fadeInUp 0.6s ease-out;
}

/* Hover effects */
.hover\:scale-105:hover {
    transform: scale(1.05);
}

/* Smooth transitions */
.transition-all {
    transition: all 0.3s ease;
}

.transition-colors {
    transition: color 0.3s ease, background-color 0.3s ease;
}
</style>
