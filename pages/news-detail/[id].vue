<template>
    <div>
        <Navbar :navlight="true" />

        <section class="relative table w-full py-32 lg:py-44 bg-no-repeat bg-center bg-cover"
            :style="{ backgroundImage: `url(${bg})` }">
            <div class="absolute inset-0 bg-black opacity-80"></div>
            <div class="container relative">
                <div class="grid grid-cols-1 text-center mt-10">
                    <h3
                        class="md:text-3xl text-2xl md:leading-snug tracking-wide leading-snug font-medium text-white mb-3">
                        {{ data && data.title ? data.title : 'WoGA News Update' }}</h3>
                    <ul class="list-none mt-6">
                        <li class="inline-block text-white/50 mx-5">
                            <span class="text-white block">Category :</span>
                            <span class="block">{{ data && data.tag ? data.tag : 'Community' }}</span>
                        </li>
                        <li class="inline-block text-white/50 mx-5">
                            <span class="text-white block">Date :</span>
                            <span class="block">{{ data && data.date ? data.date : '15th Dec 2024' }}</span>
                        </li>
                        <li class="inline-block text-white/50 mx-5">
                            <span class="text-white block">Time :</span>
                            <span class="block">5 Min Read</span>
                        </li>
                    </ul>
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

        <section class="relative md:py-24 py-16">
            <div class="container relative">
                <div class="grid lg:grid-cols-12 md:grid-cols-2 grid-cols-1 gap-6">
                    <div class="lg:col-span-8 md:order-1 order-2">
                        <div class="relative overflow-hidden rounded-xl shadow dark:shadow-gray-800">
                            <img :src="data && data.image ? data.image : newsImage" alt=""
                                class="w-full h-96 object-cover" />

                            <div class="p-8">
                                <div class="flex items-center mb-6">
                                    <span class="bg-primary text-white text-sm px-3 py-1 rounded-full mr-4">{{ data &&
                                        data.tag ? data.tag : 'Community' }}</span>
                                    <span class="text-slate-400 text-sm flex items-center">
                                        <i data-feather="calendar" class="size-4 me-2"></i>
                                        {{ data && data.date ? data.date : '15th Dec 2024' }}
                                    </span>
                                </div>

                                <h1 class="text-3xl font-bold text-gray-900 dark:text-white mb-6">
                                    {{ data && data.title ? data.title : 'WoGA News Update' }}
                                </h1>

                                <div class="prose prose-lg max-w-none text-slate-600 dark:text-slate-300">
                                    <p class="text-xl leading-relaxed mb-6">
                                        {{ data && data.excerpt ? data.excerpt : `Stay updated with the latest news and
                                        developments from our community.` }}
                                    </p>

                                    <div v-if="data && data.content"
                                        class="whitespace-pre-line leading-relaxed text-slate-700 dark:text-slate-300">
                                        {{ data.content }}
                                    </div>

                                    <template v-else>
                                        <p class="text-slate-600 dark:text-slate-300 leading-relaxed mb-6">
                                            The Wolayta Global Alliance continues to make significant strides in our
                                            mission
                                            to build bridges between communities, foster unity, and promote human rights
                                            worldwide. Our recent initiatives have brought together community members
                                            from
                                            across the globe, creating stronger connections and mutual support networks.
                                        </p>

                                        <div
                                            class="bg-gradient-to-r from-primary/10 to-blue-50 dark:from-slate-800 dark:to-slate-700 border-l-4 border-primary p-6 rounded-r-lg my-8">
                                            <p class="text-lg italic text-slate-700 dark:text-slate-300">
                                                "Together, we create opportunities, protect culture, and stand for human
                                                rights. Our community's strength lies in our unity and shared commitment
                                                to
                                                making a positive impact."
                                            </p>
                                            <p class="text-sm text-slate-500 dark:text-slate-400 mt-2">- WoGA Leadership
                                                Team</p>
                                        </div>

                                        <p class="text-slate-600 dark:text-slate-300 leading-relaxed mb-6">
                                            This year has been particularly impactful as we've expanded our programs to
                                            reach more families and individuals in need. Our cultural preservation
                                            efforts
                                            have gained momentum, with new initiatives launched to document and share
                                            our
                                            rich heritage with younger generations.
                                        </p>

                                        <h3 class="text-2xl font-semibold text-gray-900 dark:text-white mb-4">Key
                                            Highlights
                                        </h3>
                                        <ul
                                            class="list-disc list-inside space-y-2 text-slate-600 dark:text-slate-300 mb-6">
                                            <li>Expanded community support programs in three new cities</li>
                                            <li>Launched cultural heritage preservation initiative</li>
                                            <li>Provided emergency relief to 50+ families</li>
                                            <li>Organized 12 community events and workshops</li>
                                            <li>Established partnerships with local organizations</li>
                                        </ul>

                                        <p class="text-slate-600 dark:text-slate-300 leading-relaxed mb-6">
                                            Looking ahead, we remain committed to our vision of creating an environment
                                            where every community member can thrive. We invite you to join us in these
                                            efforts and be part of our growing movement for positive change.
                                        </p>

                                        <div class="bg-slate-50 dark:bg-slate-800 p-6 rounded-lg mt-8">
                                            <h4 class="text-lg font-semibold text-gray-900 dark:text-white mb-3">Stay
                                                Connected</h4>
                                            <p class="text-slate-600 dark:text-slate-300 mb-4">
                                                Follow us on social media and subscribe to our newsletter to stay
                                                updated
                                                with the latest news and events.
                                            </p>
                                            <div class="flex space-x-4">
                                                <a href="#"
                                                    class="text-primary hover:text-primary/80 transition-colors duration-300">
                                                    <i data-feather="facebook" class="size-5"></i>
                                                </a>
                                                <a href="#"
                                                    class="text-primary hover:text-primary/80 transition-colors duration-300">
                                                    <i data-feather="twitter" class="size-5"></i>
                                                </a>
                                                <a href="#"
                                                    class="text-primary hover:text-primary/80 transition-colors duration-300">
                                                    <i data-feather="linkedin" class="size-5"></i>
                                                </a>
                                                <a href="#"
                                                    class="text-primary hover:text-primary/80 transition-colors duration-300">
                                                    <i data-feather="instagram" class="size-5"></i>
                                                </a>
                                            </div>
                                        </div>
                                    </template>
                                </div>
                            </div>
                        </div>

                        <!-- Share Section -->
                        <div class="p-6 rounded-xl shadow dark:shadow-gray-800 mt-6 bg-white dark:bg-slate-900">
                            <h5 class="text-lg font-semibold mb-4">Share this article:</h5>
                            <div class="flex flex-wrap gap-4">
                                <button @click="shareOnFacebook"
                                    class="flex items-center px-4 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-colors duration-300">
                                    <i data-feather="facebook" class="size-4 mr-2"></i>
                                    Facebook
                                </button>
                                <button @click="shareOnTwitter"
                                    class="flex items-center px-4 py-2 bg-blue-400 text-white rounded-lg hover:bg-blue-500 transition-colors duration-300">
                                    <i data-feather="twitter" class="size-4 mr-2"></i>
                                    Twitter
                                </button>
                                <button @click="shareOnLinkedIn"
                                    class="flex items-center px-4 py-2 bg-blue-700 text-white rounded-lg hover:bg-blue-800 transition-colors duration-300">
                                    <i data-feather="linkedin" class="size-4 mr-2"></i>
                                    LinkedIn
                                </button>
                                <button @click="copyToClipboard"
                                    class="flex items-center px-4 py-2 bg-gray-600 text-white rounded-lg hover:bg-gray-700 transition-colors duration-300">
                                    <i data-feather="link" class="size-4 mr-2"></i>
                                    {{ copyButtonText }}
                                </button>
                            </div>
                        </div>
                    </div>

                    <div class="lg:col-span-4 md:order-2 order-1">
                        <!-- Recent News Sidebar -->
                        <div class="bg-white dark:bg-slate-900 rounded-xl shadow dark:shadow-gray-800 p-6 mb-6">
                            <h4 class="text-xl font-semibold text-gray-900 dark:text-white mb-6">Recent News</h4>
                            <div class="space-y-4">
                                <div v-for="(item, index) in recentNews" :key="index" class="flex space-x-4 group">
                                    <img :src="item.image" class="w-16 h-16 object-cover rounded-lg flex-shrink-0"
                                        alt="">
                                    <div class="flex-1">
                                        <h5
                                            class="text-sm font-medium text-gray-900 dark:text-white group-hover:text-primary transition-colors duration-300 line-clamp-2">
                                            {{ item.title }}
                                        </h5>
                                        <p class="text-xs text-slate-400 mt-1">{{ item.date }}</p>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <!-- Categories Sidebar -->
                        <!-- <div class="bg-white dark:bg-slate-900 rounded-xl shadow dark:shadow-gray-800 p-6">
                            <h4 class="text-xl font-semibold text-gray-900 dark:text-white mb-6">Categories</h4>
                            <div class="space-y-2">
                                <a v-for="category in categories" :key="category" href="#"
                                    class="block px-4 py-2 text-slate-600 dark:text-slate-300 hover:text-primary hover:bg-primary/10 rounded-lg transition-colors duration-300">
                                    {{ category }}
                                </a>
                            </div>
                        </div> -->
                    </div>
                </div>
            </div>

            <!-- Related News Section -->
            <div class="container relative md:mt-24 mt-16">
                <div class="grid grid-cols-1 pb-6 text-center">
                    <h4 class="mb-6 md:text-3xl text-2xl md:leading-normal leading-normal font-semibold">Related News
                    </h4>
                    <p class="text-slate-400 max-w-xl mx-auto">Discover more stories and updates from our community.</p>
                </div>

                <div class="grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 gap-6">
                    <div v-for="(item, index) in relatedNews" :key="index"
                        class="group relative h-fit overflow-hidden bg-white dark:bg-slate-900 rounded-xl shadow dark:shadow-gray-700 hover:shadow-xl transition-all duration-500">
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
            </div>

            <div class="container relative md:mt-24 mt-16">
                <NewsLetter />
            </div>
        </section>

        <Footer />
        <ScrollToTop />
        <Switcher />
    </div>
</template>

<script setup>
import { useRoute } from 'vue-router'
import newsImage from '@/assets/images/course/1.jpg'
import bg from '@/assets/images/bg/3.jpg'
import { newsData } from '@/data/data'

const route = useRoute()

const data = newsData.find((item) => item.id === parseInt(route.params.id))

// Copy button text state
const copyButtonText = ref('Copy Link')

// Recent news (excluding current article)
const recentNews = computed(() =>
    newsData.filter(item => item.id !== parseInt(route.params.id)).slice(0, 4)
)

// Related news (same category, excluding current article)
const relatedNews = computed(() =>
    newsData.filter(item =>
        item.id !== parseInt(route.params.id) &&
        item.tag === data?.tag
    ).slice(0, 3)
)

// Categories
const categories = [
    'Community',
    'Humanitarian',
    'Cultural',
    'Education',
    'Integration',
    'Partnership'
]

// Share functions
const shareOnFacebook = () => {
    const url = encodeURIComponent(window.location.href)
    const title = encodeURIComponent(data?.title || 'WoGA News Update')
    const shareUrl = `https://www.facebook.com/sharer/sharer.php?u=${url}&quote=${title}`
    window.open(shareUrl, '_blank', 'width=600,height=400')
}

const shareOnTwitter = () => {
    const url = encodeURIComponent(window.location.href)
    const title = encodeURIComponent(data?.title || 'WoGA News Update')
    const text = encodeURIComponent(`Check out this news from WoGA: ${title}`)
    const shareUrl = `https://twitter.com/intent/tweet?url=${url}&text=${text}`
    window.open(shareUrl, '_blank', 'width=600,height=400')
}

const shareOnLinkedIn = () => {
    const url = encodeURIComponent(window.location.href)
    const title = encodeURIComponent(data?.title || 'WoGA News Update')
    const summary = encodeURIComponent(data?.excerpt || 'Stay updated with the latest news from Wolayta Global Alliance.')
    const shareUrl = `https://www.linkedin.com/sharing/share-offsite/?url=${url}&title=${title}&summary=${summary}`
    window.open(shareUrl, '_blank', 'width=600,height=400')
}

const copyToClipboard = async () => {
    try {
        await navigator.clipboard.writeText(window.location.href)
        copyButtonText.value = 'Copied!'
        setTimeout(() => {
            copyButtonText.value = 'Copy Link'
        }, 2000)
    } catch (err) {
        // Fallback for older browsers
        const textArea = document.createElement('textarea')
        textArea.value = window.location.href
        document.body.appendChild(textArea)
        textArea.select()
        document.execCommand('copy')
        document.body.removeChild(textArea)
        copyButtonText.value = 'Copied!'
        setTimeout(() => {
            copyButtonText.value = 'Copy Link'
        }, 2000)
    }
}

// SEO
useHead({
    title: `${data?.title || 'News'} - WoGA`,
    meta: [
        { name: 'description', content: data?.excerpt || 'Stay updated with the latest news from Wolayta Global Alliance.' }
    ]
})
</script>

<style scoped>
.line-clamp-2 {
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    line-clamp: 2;
    overflow: hidden;
}

.line-clamp-3 {
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
    line-clamp: 3;
    overflow: hidden;
}
</style>
