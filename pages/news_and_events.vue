<template>
    <div>
        <Navbar :navlight="true" />

        <!-- Hero Section -->
        <section class="relative table w-full py-32 lg:py-44 bg-no-repeat bg-center bg-cover"
            :style="{ backgroundImage: `url(${bg})` }">
            <div class="absolute inset-0 bg-black opacity-80"></div>
            <div class="container relative">
                <div class="grid grid-cols-1 text-center mt-10">
                    <h3 class="md:text-4xl text-3xl md:leading-normal leading-normal font-bold text-white mb-4">News &
                        Events</h3>
                    <p class="text-lg text-gray-200 max-w-3xl mx-auto">Stay updated with the latest news, events, and
                        community activities from WoGA.</p>
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

        <!-- Featured News Section -->
        <section class="relative lg:py-24 py-16">
            <div class="container relative">
                <div class="grid grid-cols-1 pb-6 text-center">
                    <h4 class="mb-6 md:text-3xl text-2xl md:leading-normal leading-normal font-semibold">Featured News
                    </h4>
                    <p class="text-slate-400 max-w-xl mx-auto">Stay informed with the latest updates and stories from
                        our community.</p>
                </div>

                <!-- Featured News Cards -->
                <div class="grid lg:grid-cols-2 gap-8 mb-16">
                    <div v-for="(item, index) in featuredNews" :key="index"
                        class="group relative overflow-hidden bg-white dark:bg-slate-900 rounded-xl shadow dark:shadow-gray-700 hover:shadow-xl transition-all duration-500">
                        <div class="relative overflow-hidden">
                            <img :src="item.image"
                                class="w-full h-64 object-cover group-hover:scale-105 transition-transform duration-500"
                                alt="">
                            <div class="absolute top-6 left-6">
                                <span class="bg-primary text-white text-sm px-3 py-1 rounded-full">{{ item.tag }}</span>
                            </div>
                        </div>

                        <div class="relative p-8">
                            <div class="flex items-center mb-4">
                                <span class="text-slate-400 text-sm flex items-center">
                                    <i data-feather="calendar" class="size-4 me-2"></i> {{ item.date }}
                                </span>
                            </div>

                            <h3
                                class="text-xl font-semibold text-gray-900 dark:text-white mb-4 group-hover:text-primary transition-colors duration-300">
                                {{ item.title }}
                            </h3>

                            <p class="text-slate-400 mb-6 leading-relaxed">{{ item.excerpt }}</p>

                            <NuxtLink :to="`/news-detail/${item.id}`"
                                class="btn btn-link hover:text-primary after:bg-primary duration-500 ease-in-out">
                                Read More <i class="mdi mdi-arrow-right"></i>
                            </NuxtLink>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- News & Events Tabs -->
        <section class="relative lg:py-24 py-16 bg-gray-50 dark:bg-slate-900">
            <div class="container relative">
                <!-- Tab Navigation -->
                <div class="flex flex-wrap justify-center mb-12">
                    <button v-for="tab in tabs" :key="tab.id" @click="activeTab = tab.id" :class="[
                        'px-6 py-3 mx-2 mb-2 rounded-lg font-medium transition-all duration-300',
                        activeTab === tab.id
                            ? 'bg-primary text-white shadow-lg'
                            : 'bg-white dark:bg-slate-800 text-gray-700 dark:text-gray-300 hover:bg-primary hover:text-white'
                    ]">
                        {{ tab.name }}
                    </button>
                </div>

                <!-- News Tab Content -->
                <div v-if="activeTab === 'news'" class="grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 gap-6">
                    <div v-for="(item, index) in regularNews" :key="index"
                        class="group relative h-fit overflow-hidden bg-white dark:bg-slate-800 rounded-xl shadow dark:shadow-gray-700 hover:shadow-xl transition-all duration-500">
                        <div class="relative overflow-hidden">
                            <img :src="item.image"
                                class="w-full h-48 object-cover group-hover:scale-105 transition-transform duration-500"
                                alt="">
                            <div class="absolute top-4 left-4">
                                <span class="bg-primary text-white text-xs px-2 py-1 rounded-full">{{ item.tag }}</span>
                            </div>
                        </div>

                        <div class="relative p-6">
                            <div class="flex justify-between mb-4">
                                <span class="text-slate-400 text-sm flex items-center">
                                    <i data-feather="calendar" class="size-4 me-1"></i> {{ item.date }}
                                </span>
                            </div>

                            <h3
                                class="text-lg font-semibold text-gray-900 dark:text-white mb-3 group-hover:text-primary transition-colors duration-300">
                                {{ item.title }}
                            </h3>

                            <p class="text-slate-400 text-sm mb-4 line-clamp-3">{{ item.excerpt }}</p>

                            <NuxtLink :to="`/news-detail/${item.id}`"
                                class="btn btn-link hover:text-primary after:bg-primary duration-500 ease-in-out text-sm">
                                Read More <i class="mdi mdi-arrow-right"></i>
                            </NuxtLink>
                        </div>
                    </div>
                </div>

                <!-- Events Tab Content -->
                <div v-if="activeTab === 'events'" class="space-y-8">
                    <!-- Upcoming Events -->
                    <div>
                        <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-6 flex items-center">
                            <svg class="w-6 h-6 mr-3 text-primary" fill="none" stroke="currentColor"
                                viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z">
                                </path>
                            </svg>
                            Upcoming Events
                        </h3>
                        <div class="grid lg:grid-cols-2 gap-6">
                            <div v-for="(event, index) in upcomingEvents" :key="index"
                                class="group relative overflow-hidden bg-white dark:bg-slate-800 rounded-xl shadow dark:shadow-gray-700 hover:shadow-xl transition-all duration-500">
                                <div class="relative overflow-hidden">
                                    <img :src="event.image"
                                        class="w-full h-48 object-cover group-hover:scale-105 transition-transform duration-500"
                                        alt="">
                                    <div class="absolute top-4 left-4">
                                        <span class="bg-green-500 text-white text-xs px-2 py-1 rounded-full">{{
                                            event.type }}</span>
                                    </div>
                                </div>

                                <div class="relative p-6">
                                    <h3
                                        class="text-xl font-semibold text-gray-900 dark:text-white mb-3 group-hover:text-primary transition-colors duration-300">
                                        {{ event.title }}
                                    </h3>

                                    <div class="space-y-2 mb-4">
                                        <div class="flex items-center text-slate-400 text-sm">
                                            <i data-feather="calendar" class="size-4 me-2"></i>
                                            {{ event.date }}
                                        </div>
                                        <div class="flex items-center text-slate-400 text-sm">
                                            <i data-feather="clock" class="size-4 me-2"></i>
                                            {{ event.time }}
                                        </div>
                                        <div class="flex items-center text-slate-400 text-sm">
                                            <i data-feather="map-pin" class="size-4 me-2"></i>
                                            {{ event.location }}
                                        </div>
                                        <div class="flex items-center text-slate-400 text-sm">
                                            <i data-feather="users" class="size-4 me-2"></i>
                                            {{ event.capacity }}
                                        </div>
                                    </div>

                                    <p class="text-slate-400 text-sm mb-4 line-clamp-2">{{ event.description }}</p>

                                    <!-- <div class="flex justify-between items-center">
                                        <span class="text-primary font-semibold">{{ event.registration }}</span>
                                        <button
                                            class="btn btn-sm bg-primary text-white hover:bg-primary/90 transition-colors duration-300">
                                            Register
                                        </button>
                                    </div> -->
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Past Events -->
                    <div>
                        <h3 v-if="pastEvents.length > 0"
                            class="text-2xl font-bold text-gray-900 dark:text-white mb-6 flex items-center">
                            <svg class="w-6 h-6 mr-3 text-slate-400" fill="none" stroke="currentColor"
                                viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M9 5H7a2 2 0 00-2 2v10a2 2 0 002 2h8a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2">
                                </path>
                            </svg>
                            Past Events
                        </h3>
                        <div class="grid lg:grid-cols-3 md:grid-cols-2 gap-6">
                            <div v-for="(event, index) in pastEvents" :key="index"
                                class="group relative overflow-hidden bg-white dark:bg-slate-800 rounded-xl shadow dark:shadow-gray-700 hover:shadow-xl transition-all duration-500">
                                <div class="relative overflow-hidden">
                                    <img :src="event.image"
                                        class="w-full h-40 object-cover group-hover:scale-105 transition-transform duration-500"
                                        alt="">
                                    <div class="absolute top-4 left-4">
                                        <span class="bg-slate-500 text-white text-xs px-2 py-1 rounded-full">{{
                                            event.type }}</span>
                                    </div>
                                </div>

                                <div class="relative p-4">
                                    <h3
                                        class="text-lg font-semibold text-gray-900 dark:text-white mb-2 group-hover:text-primary transition-colors duration-300">
                                        {{ event.title }}
                                    </h3>

                                    <div class="space-y-1 mb-3">
                                        <div class="flex items-center text-slate-400 text-xs">
                                            <i data-feather="calendar" class="size-3 me-1"></i>
                                            {{ event.date }}
                                        </div>
                                        <div class="flex items-center text-slate-400 text-xs">
                                            <i data-feather="map-pin" class="size-3 me-1"></i>
                                            {{ event.location }}
                                        </div>
                                    </div>

                                    <p class="text-slate-400 text-xs line-clamp-2">{{ event.description }}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Newsletter Section -->
        <section class="relative lg:py-24 py-16">
            <div class="container relative">
                <NewsLetter />
            </div>
        </section>

        <Footer />
        <ScrollToTop />
        <Switcher />
    </div>
</template>

<script setup>
import bg from '@/assets/images/bg/2.jpg'
import { newsData, eventsData } from '@/data/data'

// Reactive data
const activeTab = ref('events')

// Tab configuration
const tabs = [
    { id: 'events', name: 'Events' },
    { id: 'news', name: 'Latest News' }
]

// Computed properties
const featuredNews = computed(() => newsData.filter(item => item.featured))
const regularNews = computed(() => newsData.filter(item => !item.featured))
const upcomingEvents = computed(() => eventsData.filter(event => event.status === 'upcoming'))
const pastEvents = computed(() => eventsData.filter(event => event.status === 'past'))

// SEO
useHead({
    title: 'News & Events - WoGA',
    meta: [
        { name: 'description', content: 'Stay updated with the latest news, events, and community activities from Wolayta Global Alliance (WoGA).' }
    ]
})
</script>

<style scoped>
.line-clamp-2 {
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
}

.line-clamp-3 {
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
    overflow: hidden;
}
</style>
