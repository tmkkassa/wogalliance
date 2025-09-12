<template>
    <div>
        <Navbar />

        <section class="relative py-5 bg-slate-50 dark:bg-slate-800 mt-[74px]">
            <div class="container relative">
                <div class="grid md:grid-cols-12 grid-cols-1 gap-2 items-center">
                    <div class="lg:col-span-5 md:col-span-4">
                        <h3 class="text-2xl md:leading-normal leading-normal font-semibold">Courses</h3>
                    </div>

                    <div class="lg:col-span-7 md:col-span-8 md:text-end">
                        <ul class="tracking-[0.5px] mb-0 inline-block">
                            <li
                                class="inline-block text-slate-400 dark:text-white/60 duration-500 ease-in-out hover:text-primary dark:hover:text-white">
                                <NuxtLink to="/">Edupath</NuxtLink>
                            </li>
                            <li
                                class="inline-block text-slate-500 dark:text-white/60 mx-0.5 ltr:rotate-0 rtl:rotate-180">
                                <i class="iconoir-nav-arrow-right align-middle"></i></li>
                            <li
                                class="inline-block text-slate-400 dark:text-white/60 duration-500 ease-in-out hover:text-primary dark:hover:text-white">
                                <NuxtLink :to="[]">Courses</NuxtLink>
                            </li>
                            <li
                                class="inline-block text-slate-500 dark:text-white/60 mx-0.5 ltr:rotate-0 rtl:rotate-180">
                                <i class="iconoir-nav-arrow-right align-middle"></i></li>
                            <li class="inline-block text-primary dark:text-white" aria-current="page">Youtube Listing
                                Courses</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <section class="relative py-12">
            <div class="container relative">
                <div class="grid lg:grid-cols-12 md:grid-cols-2 grid-cols-1 gap-6">
                    <div class="lg:col-span-8 md:order-1 order-2">
                        <div class="grid lg:grid-cols-2 grid-cols-1 gap-6">
                            <div v-for="(item, index) in youtubeList" :key="index"
                                class="group bg-white dark:bg-slate-900 rounded-md shadow-md hover:shadow-lg shadow-slate-100 dark:shadow-slate-800 transition duration-500">
                                <div class="p-3 pb-0 relative">
                                    <iframe :src="item.video" allow="autoplay; encrypted-media"
                                        class="w-full rounded-md h-44" allowfullscreen=""></iframe>
                                    <div class="absolute start-6 top-6">
                                        <span
                                            class="bg-primary text-white text-[12px] px-2.5 py-1 rounded-md h-4 mx-[2px]">{{ item.tag1 }}</span>
                                        <span
                                            class="bg-primary text-white text-[12px] px-2.5 py-1 rounded-md h-4 mx-[2px]">{{ item.tag2 }}</span>
                                    </div>

                                    <div class="absolute -bottom-5 end-6">
                                        <span
                                            class="bg-primary text-white size-10 flex items-center justify-center rounded-full shadow-md shadow-slate-100 dark:shadow-slate-800 font-semibold">${{ item.amount }}</span>
                                    </div>
                                </div>

                                <div class="p-6">
                                    <div class="flex mb-3">
                                        <span class="text-slate-400 text-sm flex items-center"><i data-feather="book"
                                                class="text-slate-900 dark:text-white size-[14px] me-1"></i>{{ item.lessons }}
                                            Lessons</span>
                                        <span class="text-slate-400 text-sm flex items-center ms-3"><i
                                                data-feather="users"
                                                class="text-slate-900 dark:text-white size-[14px] me-1"></i>{{ item.students }}
                                            Students</span>
                                    </div>

                                    <NuxtLink to="/course-detail" class="text-lg hover:text-primary font-medium">
                                        {{ item.title }}</NuxtLink>

                                    <p class="text-slate-400 mt-2">{{ item.desc }}</p>

                                    <div class="flex justify-between mt-3">
                                        <span class="flex items-center"><img :src="item.user"
                                                class="size-8 rounded-full shadow shadow-slate-100 dark:shadow-slate-800 me-2"
                                                alt="">
                                            <NuxtLink :to="[]" class="hover:text-primary font-medium"> {{ item.name }}
                                            </NuxtLink>
                                        </span>
                                        <NuxtLink :to="[]"
                                            class="h-8 px-3 tracking-wide inline-flex items-center justify-center font-medium rounded-md bg-primary/10 hover:bg-primary text-primary hover:text-white text-sm">
                                            Explore <i class="mdi mdi-arrow-right align-middle ms-1"></i></NuxtLink>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="grid md:grid-cols-12 grid-cols-1 mt-6">
                            <div class="md:col-span-12 text-center">
                                <nav>
                                    <ul class="inline-flex items-center -space-x-px">
                                        <li>
                                            <NuxtLink :to="[]"
                                                class="size-8 inline-flex justify-center items-center mx-1 rounded-full text-slate-400 bg-white dark:bg-slate-900 hover:text-white shadow-sm shadow-slate-100 dark:shadow-slate-800 hover:border-primary dark:hover:border-primary hover:bg-primary dark:hover:bg-primary">
                                                <i class="mdi mdi-chevron-left text-[20px]"></i>
                                            </NuxtLink>
                                        </li>
                                        <li>
                                            <NuxtLink :to="[]"
                                                class="size-8 inline-flex justify-center items-center mx-1 rounded-full text-slate-400 hover:text-white bg-white dark:bg-slate-900 shadow-sm shadow-slate-100 dark:shadow-slate-800 hover:border-primary dark:hover:border-primary hover:bg-primary dark:hover:bg-primary">
                                                1</NuxtLink>
                                        </li>
                                        <li>
                                            <NuxtLink :to="[]"
                                                class="size-8 inline-flex justify-center items-center mx-1 rounded-full text-slate-400 hover:text-white bg-white dark:bg-slate-900 shadow-sm shadow-slate-100 dark:shadow-slate-800 hover:border-primary dark:hover:border-primary hover:bg-primary dark:hover:bg-primary">
                                                2</NuxtLink>
                                        </li>
                                        <li>
                                            <NuxtLink :to="[]" aria-current="page"
                                                class="z-10 size-8 inline-flex justify-center items-center mx-1 rounded-full text-white bg-primary shadow-sm shadow-slate-100 dark:shadow-slate-800">
                                                3</NuxtLink>
                                        </li>
                                        <li>
                                            <NuxtLink :to="[]"
                                                class="size-8 inline-flex justify-center items-center mx-1 rounded-full text-slate-400 hover:text-white bg-white dark:bg-slate-900 shadow-sm shadow-slate-100 dark:shadow-slate-800 hover:border-primary dark:hover:border-primary hover:bg-primary dark:hover:bg-primary">
                                                4</NuxtLink>
                                        </li>
                                        <li>
                                            <NuxtLink :to="[]"
                                                class="size-8 inline-flex justify-center items-center mx-1 rounded-full text-slate-400 bg-white dark:bg-slate-900 hover:text-white shadow-sm shadow-slate-100 dark:shadow-slate-800 hover:border-primary dark:hover:border-primary hover:bg-primary dark:hover:bg-primary">
                                                <i class="mdi mdi-chevron-right text-[20px]"></i>
                                            </NuxtLink>
                                        </li>
                                    </ul>
                                </nav>
                            </div>
                        </div>
                    </div>

                    <div class="lg:col-span-4 md:order-2 order-1">
                        <CoursesSidebar />
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
import { youtubeList } from '@/data/data';
</script>