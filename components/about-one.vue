<template>
    <div class="grid md:grid-cols-12 grid-cols-1 items-center gap-6">
        <div class="lg:col-span-6 md:col-span-7">
            <div class="relative">
                <div class="relative md:shrink-0 lg:me-0 me-10">
                    <img class="object-cover md:w-96 w-84 h-[500px] rounded-lg shadow-md dark:shadow-gyay-700"
                        :src="about1" alt="" />
                </div>

                <div class="absolute bottom-10 lg:end-6 end-0">

                    <div class="relative md:shrink-0">
                        <img class="object-cover size-48 rounded-lg shadow-md dark:shadow-gyay-700" :src="about2"
                            alt="" />
                    </div>
                </div>
            </div>
        </div>

        <div class="lg:col-span-6 md:col-span-5">
            <span v-if="title" class="text-primary font-semibold mb-3 uppercase">Our Story</span>
            <h4 class="mb-4 md:text-3xl text-2xl md:leading-normal leading-normal font-semibold">Building Community,
                <br> Preserving Culture
            </h4>
            <p class="text-slate-400 max-w-xl mx-auto">
                We are Wolayta Global Alliance (WoGA) — a community-driven nonprofit dedicated to supporting immigrants’
                integration, strengthening Wolayta cultural identity, and promoting humanitarian action and human
                rights. <br><br>

                Through networking, solidarity, and self-help initiatives, we empower Wolayta immigrants in the U.S. and
                abroad while staying connected to our community of origin in Ethiopia. <br><br>

                You can be part of this journey by joining our alliance, volunteering your skills, or supporting our
                humanitarian and cultural programs through donations.
            </p>

            <div class="mt-6">
                <NuxtLink to="/aboutus"
                    class="h-10 px-5 tracking-wide inline-flex items-center justify-center font-medium rounded-md bg-primary/10 hover:bg-primary text-primary hover:text-white transition-colors duration-300 shadow-md hover:shadow-lg">
                    Learn More <i class="mdi mdi-arrow-right align-middle ms-1"></i></NuxtLink>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref, defineProps } from 'vue';
import about1 from '@/assets/images/course/1.jpg'
import about2 from '@/assets/images/course/2.jpg'

defineProps({
    title: Boolean
})

const open = ref(false)

const toggle = () => {
    open.value = !open.value
}
</script>
