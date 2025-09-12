<template>
    <div class="grid lg:grid-cols-4 md:grid-cols-2 grid-cols-1 mt-6 gap-6">
        <div v-for="(item, index) in featureData" :key="index"
            class="p-6 shadow-lg shadow-slate-100 dark:shadow-slate-800 transition duration-500 rounded-2xl">
            <div
                class="size-16 bg-primary/5 text-primary rounded-2xl flex align-middle justify-center items-center shadow-sm hover:shadow-md transition-shadow duration-300">
                <i class="text-3xl" :class="item.icon"></i>
            </div>

            <div class="content mt-6">
                <NuxtLink :to="[]"
                    class="text-lg hover:text-primary dark:text-white dark:hover:text-primary transition-all duration-500 ease-in-out font-semibold">
                    {{ item.title }}</NuxtLink>
                <p class="text-slate-400 mt-3">{{ item.desc }}</p>

                <!-- <div class="mt-3">
                    <NuxtLink :to="[]" class="hover:text-primary dark:hover:text-primary after:bg-primary dark:text-white transition duration-500">Read More <i class="mdi mdi-arrow-right"></i></NuxtLink>
                </div> -->
            </div>
        </div>
    </div>
</template>

<script setup>
import { featureData } from '@/data/data';
</script>
