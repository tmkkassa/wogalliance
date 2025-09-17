<template>
    <div>
        <Navbar :navlight="true" />

        <!-- Hero Section -->
        <section class="relative table w-full py-32 lg:py-44 bg-no-repeat bg-center bg-cover"
            :style="{ backgroundImage: `url(${bg})` }">
            <div class="absolute inset-0 bg-black opacity-80"></div>
            <div class="container relative">
                <div class="grid grid-cols-1 text-center mt-10">
                    <h3 class="md:text-4xl text-3xl md:leading-normal leading-normal font-bold text-white mb-4">Cultural
                        Gallery</h3>
                    <p class="text-lg text-gray-200 max-w-3xl mx-auto">Explore our rich heritage through photos and
                        videos
                        showcasing Wolayta culture, history, and traditions.</p>
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

        <!-- Gallery Section -->
        <section class="relative lg:py-24 py-16">
            <div class="container relative max-w-7xl mx-auto px-4">
                <div class="grid grid-cols-12 gap-6">
                    <!-- Sidebar -->
                    <div class="col-span-12 lg:col-span-3">
                        <div class="sticky top-24 space-y-6">
                            <!-- Filter Categories -->
                            <div class="bg-white dark:bg-slate-900 rounded-xl shadow dark:shadow-gray-700 p-6">
                                <h4 class="text-lg font-semibold text-gray-900 dark:text-white mb-6 flex items-center">
                                    <i data-feather="filter" class="w-5 h-5 mr-2 text-primary"></i>
                                    Filter by Category
                                </h4>
                                <div class="space-y-3">
                                    <button v-for="category in categories" :key="category.id"
                                        @click="filterByCategory(category.id)" :class="[
                                            'w-full text-left px-4 py-3 rounded-lg transition-all duration-300 flex items-center justify-between group',
                                            activeFilter === category.id
                                                ? 'bg-primary text-white shadow-lg'
                                                : 'bg-gray-50 dark:bg-slate-800 text-gray-700 dark:text-gray-300 hover:bg-primary hover:text-white'
                                        ]">
                                        <div class="flex items-center">
                                            <i :data-feather="category.icon" class="w-4 h-4 mr-3"></i>
                                            <span class="font-medium text-sm">{{ category.name }}</span>
                                        </div>
                                        <span :class="[
                                            'text-xs px-2 py-1 rounded-full',
                                            activeFilter === category.id
                                                ? 'bg-white/20 text-white'
                                                : 'bg-primary/10 text-primary group-hover:bg-white/20 group-hover:text-white'
                                        ]">
                                            {{ getCategoryCount(category.id) }}
                                        </span>
                                    </button>
                                </div>
                            </div>

                            <!-- Search Box -->
                            <!-- <div class="bg-white dark:bg-slate-900 rounded-xl shadow dark:shadow-gray-700 p-6">
                                <h4 class="text-lg font-semibold text-gray-900 dark:text-white mb-6 flex items-center">
                                    <i data-feather="search" class="w-5 h-5 mr-2 text-primary"></i>
                                    Search Gallery
                                </h4>
                                <div class="relative">
                                    <input v-model="searchQuery" type="text"
                                        class="w-full px-4 py-3 pl-10 border border-gray-200 dark:border-slate-700 rounded-lg bg-gray-50 dark:bg-slate-800 text-gray-900 dark:text-white focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent"
                                        placeholder="Search photos and videos...">
                                    <i data-feather="search" class="absolute left-3 top-3.5 w-4 h-4 text-gray-400"></i>
                                </div>
                            </div> -->

                            <!-- Type Filter -->
                            <!-- <div class="bg-white dark:bg-slate-900 rounded-xl shadow dark:shadow-gray-700 p-6">
                                <h4 class="text-lg font-semibold text-gray-900 dark:text-white mb-6 flex items-center">
                                    <i data-feather="image" class="w-5 h-5 mr-2 text-primary"></i>
                                    Media Type
                                </h4>
                                <div class="space-y-3">
                                    <button v-for="type in mediaTypes" :key="type.id" @click="filterByType(type.id)"
                                        :class="[
                                            'w-full text-left px-4 py-3 rounded-lg transition-all duration-300 flex items-center',
                                            activeTypeFilter === type.id
                                                ? 'bg-primary text-white'
                                                : 'text-gray-700 dark:text-gray-300 hover:bg-primary hover:text-white'
                                        ]">
                                        <i :data-feather="type.icon" class="w-4 h-4 mr-3"></i>
                                        <span class="text-sm">{{ type.name }}</span>
                                        <span class="ml-auto text-xs">{{ getTypeCount(type.id) }}</span>
                                    </button>
                                </div>
                            </div> -->
                        </div>
                    </div>

                    <!-- Gallery Content -->
                    <div class=" col-span-12 lg:col-span-9">
                        <!-- Results Header -->
                        <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between mb-8">
                            <div>
                                <h4 class="text-2xl font-bold text-gray-900 dark:text-white mb-2">
                                    {{ filteredItems.length }} {{ filteredItems.length === 1 ? 'Item' : 'Items' }} Found
                                </h4>
                                <p class="text-slate-400">
                                    <span v-if="activeFilter !== 'all'">
                                        Showing {{ getActiveCategoryName() }} content
                                    </span>
                                    <span v-else>Showing all gallery items</span>
                                    <span v-if="searchQuery"> matching "{{ searchQuery }}"</span>
                                </p>
                            </div>
                            <div class="flex items-center space-x-4 mt-4 sm:mt-0">
                                <!-- View Toggle -->
                                <div class="flex bg-gray-100 dark:bg-slate-800 rounded-lg p-1">
                                    <button @click="viewMode = 'grid'" :class="[
                                        'px-3 py-2 rounded-md text-sm font-medium transition-all duration-300',
                                        viewMode === 'grid'
                                            ? 'bg-primary text-white shadow-sm'
                                            : 'text-gray-600 dark:text-gray-400 hover:text-primary'
                                    ]">
                                        <i data-feather="grid" class="w-4 h-4"></i>
                                    </button>
                                    <button @click="viewMode = 'list'" :class="[
                                        'px-3 py-2 rounded-md text-sm font-medium transition-all duration-300',
                                        viewMode === 'list'
                                            ? 'bg-primary text-white shadow-sm'
                                            : 'text-gray-600 dark:text-gray-400 hover:text-primary'
                                    ]">
                                        <i data-feather="list" class="w-4 h-4"></i>
                                    </button>
                                </div>
                            </div>
                        </div>

                        <!-- Gallery Grid -->
                        <div v-if="filteredItems.length > 0" :class="[
                            'transition-all duration-500',
                            viewMode === 'grid'
                                ? 'grid xl:grid-cols-3 lg:grid-cols-2 md:grid-cols-2 gap-8'
                                : 'space-y-8'
                        ]">
                            <div v-for="item in filteredItems" :key="item.id" :class="[
                                'group relative overflow-hidden bg-white dark:bg-slate-900 rounded-xl shadow dark:shadow-gray-700 hover:shadow-xl transition-all duration-500',
                                viewMode === 'list' ? 'flex' : ''
                            ]">
                                <!-- Media Content -->
                                <div :class="[
                                    'relative overflow-hidden',
                                    viewMode === 'list' ? 'w-1/3 h-56' : 'h-56'
                                ]" @click="openModal(item)" class="cursor-pointer">
                                    <!-- Video Overlay -->
                                    <div v-if="item.type === 'video'"
                                        class="absolute inset-0 flex items-center justify-center bg-black/20 z-10">
                                        <div
                                            class="w-16 h-16 bg-white/90 rounded-full flex items-center justify-center group-hover:scale-110 transition-transform duration-300">
                                            <i data-feather="play" class="w-8 h-8 text-primary ml-1"></i>
                                        </div>
                                    </div>
                                    <img v-if="item.type === 'image'" :src="item.image" :class="[
                                        'w-full h-full object-cover group-hover:scale-105 transition-transform duration-500',
                                        viewMode === 'list' ? 'object-center' : ''
                                    ]" alt="">
                                    <div v-else class="w-full h-full bg-black"></div>

                                    <!-- Type Badge -->
                                    <div class="absolute top-4 left-4">
                                        <span :class="[
                                            'px-2 py-1 rounded-full text-xs font-medium',
                                            item.type === 'video'
                                                ? 'bg-red-500 text-white'
                                                : 'bg-primary text-white'
                                        ]">
                                            <i :data-feather="item.type === 'video' ? 'video' : 'image'"
                                                class="w-3 h-3 inline mr-1"></i>
                                            {{ item.type }}
                                        </span>
                                    </div>

                                    <!-- Category Badge -->
                                    <div class="absolute top-4 right-4">
                                        <span
                                            class="bg-white/90 dark:bg-slate-800/90 text-gray-700 dark:text-gray-300 px-2 py-1 rounded-full text-xs font-medium">
                                            {{ getCategoryDisplayName(item.category) }}
                                        </span>
                                    </div>
                                </div>

                                <!-- Content -->
                                <div :class="[
                                    'relative p-6',
                                    viewMode === 'list' ? 'flex-1' : ''
                                ]">
                                    <!-- <div class="flex items-center mb-3">
                                        <span class="text-slate-400 text-sm flex items-center">
                                            <i data-feather="calendar" class="size-4 me-2"></i> {{ item.date }}
                                        </span>
                                    </div> -->

                                    <!-- <h3
                                        class="text-xl font-semibold text-gray-900 dark:text-white mb-3 group-hover:text-primary transition-colors duration-300">
                                        {{ item.title }}
                                    </h3> -->

                                    <p class="text-slate-400 mb-4 leading-relaxed"
                                        :class="viewMode === 'list' ? '' : 'line-clamp-2'">
                                        {{ item.description }}
                                    </p>

                                    <!-- Tags -->
                                    <!-- <div class="flex flex-wrap gap-2 mb-4">
                                        <span v-for="tag in item.tags.slice(0, 3)" :key="tag"
                                            class="px-2 py-1 bg-gray-100 dark:bg-slate-800 text-gray-600 dark:text-gray-400 rounded-md text-xs">
                                            #{{ tag }}
                                        </span>
                                    </div> -->

                                    <!-- Action Button removed; click media opens modal -->
                                </div>
                            </div>
                        </div>

                        <!-- No Results -->
                        <div v-else class="text-center py-16">
                            <div
                                class="w-24 h-24 bg-gray-100 dark:bg-slate-800 rounded-full flex items-center justify-center mx-auto mb-6">
                                <i data-feather="search" class="w-12 h-12 text-gray-400"></i>
                            </div>
                            <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">No items found</h3>
                            <p class="text-slate-400 mb-6">Try adjusting your search or filter criteria</p>
                            <button @click="clearFilters"
                                class="btn bg-primary text-white hover:bg-primary/90 transition-colors duration-300">
                                Clear Filters
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Modal -->
        <div v-if="selectedItem" class="fixed inset-0 bg-black/80 z-50 flex items-center justify-center p-4"
            @click="closeModal">
            <div class="bg-white dark:bg-slate-900 rounded-xl max-w-6xl w-full max-h-[90vh] overflow-y-auto"
                @click.stop>
                <div class="relative">
                    <!-- Close Button -->
                    <button @click="closeModal"
                        class="absolute top-4 right-4 z-10 w-10 h-10 bg-black/60 text-white rounded-full flex items-center justify-center hover:bg-black/80 transition-colors duration-300">
                        <i class="mdi mdi-close text-xl"></i>
                    </button>

                    <!-- Modal Content -->
                    <div class="grid lg:grid-cols-2 gap-0">
                        <!-- Media -->
                        <div class="relative">
                            <img v-if="selectedItem.type === 'image'" :src="selectedItem.image"
                                class="w-full h-96 xl:h-full object-cover rounded-l-xl" alt="">

                            <!-- Video Embed -->
                            <div v-else class="w-full h-96 xl:h-full bg-black rounded-l-xl overflow-hidden">
                                <iframe v-if="selectedItem.videoUrl" class="w-full h-full"
                                    :src="selectedItem.videoUrl + '?rel=0&modestbranding=1'"
                                    title="YouTube video player" frameborder="0"
                                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                                    referrerpolicy="strict-origin-when-cross-origin" allowfullscreen>
                                </iframe>
                                <div v-else class="w-full h-full flex items-center justify-center text-white">
                                    <span>Video unavailable</span>
                                </div>
                            </div>
                        </div>

                        <!-- Details -->
                        <div class="p-8">
                            <div class="flex items-center mb-4">
                                <span :class="[
                                    'px-3 py-1 rounded-full text-sm font-medium mr-3',
                                    selectedItem.type === 'video'
                                        ? 'bg-red-500 text-white'
                                        : 'bg-primary text-white'
                                ]">
                                    <i :data-feather="selectedItem.type === 'video' ? 'video' : 'image'"
                                        class="w-4 h-4 inline mr-1"></i>
                                    {{ selectedItem.type }}
                                </span>
                                <!-- <span class="text-slate-400 text-sm flex items-center">
                                    <i data-feather="calendar" class="size-4 me-2"></i> {{ selectedItem.date }}
                                </span> -->
                            </div>

                            <!-- <h2 class="text-2xl font-bold text-gray-900 dark:text-white mb-4">
                                {{ selectedItem.title }}
                            </h2> -->

                            <p class="text-slate-400 mb-6 leading-relaxed">
                                {{ selectedItem.description }}
                            </p>

                            <!-- Category -->
                            <div class="mb-6">
                                <h4 class="text-sm font-semibold text-gray-900 dark:text-white mb-2">Category</h4>
                                <span
                                    class="inline-block px-3 py-1 bg-gray-100 dark:bg-slate-800 text-gray-700 dark:text-gray-300 rounded-full text-sm">
                                    {{ getCategoryDisplayName(selectedItem.category) }}
                                </span>
                            </div>

                            <!-- Tags -->
                            <div class="mb-6">
                                <h4 class="text-sm font-semibold text-gray-900 dark:text-white mb-2">Tags</h4>
                                <div class="flex flex-wrap gap-2">
                                    <span v-for="tag in selectedItem.tags" :key="tag"
                                        class="px-3 py-1 bg-primary/10 text-primary rounded-full text-sm">
                                        #{{ tag }}
                                    </span>
                                </div>
                            </div>

                            <!-- Action Buttons -->
                            <!-- <div class="flex space-x-4">
                                <button
                                    class="btn bg-primary text-white hover:bg-primary/90 transition-colors duration-300">
                                    <i data-feather="download" class="w-4 h-4 mr-2"></i>
                                    Download
                                </button>
                                <button
                                    class="btn bg-gray-100 dark:bg-slate-800 text-gray-700 dark:text-gray-300 hover:bg-gray-200 dark:hover:bg-slate-700 transition-colors duration-300">
                                    <i data-feather="share-2" class="w-4 h-4 mr-2"></i>
                                    Share
                                </button>
                            </div> -->
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <Footer />
        <!-- <ScrollToTop /> -->
        <!-- <Switcher /> -->
    </div>
</template>

<script setup>
import bg from '@/assets/images/gallery/ajora3.jpeg'
import { galleryData } from '@/data/data'
import feather from 'feather-icons'

// Reactive data
const activeFilter = ref('all')
const activeTypeFilter = ref('all')
const searchQuery = ref('')
const viewMode = ref('grid')
const selectedItem = ref(null)

// Categories configuration
const categories = [
    { id: 'all', name: 'All', icon: 'grid' },
    { id: 'historical archives', name: 'Historical Archives', icon: 'archive' },
    { id: 'historical sites and artifacts', name: 'Historical Sites & Artifacts', icon: 'map-pin' },
    { id: 'gifata celebration', name: 'Gifata Celebration', icon: 'calendar' },
    { id: 'cultural costumes', name: 'Cultural Costumes', icon: 'user' },
    { id: 'tourist sites and attractions', name: 'Tourist Sites & Attractions', icon: 'camera' }
]

// Media types
const mediaTypes = [
    { id: 'all', name: 'All Media', icon: 'grid' },
    { id: 'image', name: 'Photos', icon: 'image' },
    { id: 'video', name: 'Videos', icon: 'video' }
]

// Computed properties
const filteredItems = computed(() => {
    let items = galleryData

    // Filter by category
    if (activeFilter.value !== 'all') {
        items = items.filter(item => item.category === activeFilter.value)
    }

    // Filter by type
    if (activeTypeFilter.value !== 'all') {
        items = items.filter(item => item.type === activeTypeFilter.value)
    }

    // Filter by search query
    if (searchQuery.value) {
        const query = searchQuery.value.toLowerCase()
        items = items.filter(item =>
            item.title.toLowerCase().includes(query) ||
            item.description.toLowerCase().includes(query) ||
            item.tags.some(tag => tag.toLowerCase().includes(query))
        )
    }

    return items
})

// Methods
const filterByCategory = (categoryId) => {
    activeFilter.value = categoryId
}

const filterByType = (typeId) => {
    activeTypeFilter.value = typeId
}

const clearFilters = () => {
    activeFilter.value = 'all'
    activeTypeFilter.value = 'all'
    searchQuery.value = ''
}

const getCategoryCount = (categoryId) => {
    if (categoryId === 'all') return galleryData.length
    return galleryData.filter(item => item.category === categoryId).length
}

const getTypeCount = (typeId) => {
    if (typeId === 'all') return galleryData.length
    return galleryData.filter(item => item.type === typeId).length
}

const getActiveCategoryName = () => {
    const category = categories.find(cat => cat.id === activeFilter.value)
    return category ? category.name : 'All'
}

const getCategoryDisplayName = (category) => {
    const categoryObj = categories.find(cat => cat.id === category)
    return categoryObj ? categoryObj.name : category
}

const openModal = (item) => {
    selectedItem.value = item
}

const closeModal = () => {
    selectedItem.value = null
}

// Initialize Feather icons
onMounted(() => {
    feather.replace()
})

// SEO
useHead({
    title: 'Cultural Gallery - WoGA',
    meta: [
        { name: 'description', content: 'Explore our rich heritage through photos and videos showcasing Wolayta culture, history, and traditions.' }
    ]
})
</script>

<style scoped>
.line-clamp-2 {
    display: -webkit-box;
    -webkit-line-clamp: 2;
    line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
}

.sticky {
    position: sticky;
    top: 6rem;
}
</style>
