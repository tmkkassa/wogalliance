<template>
    <section class="swiper mySwiper swiper-slider-hero relative block h-screen overflow-hidden" id="home">
        <swiper class="swiper-wrapper" :slides-per-view="1" :modules="[Autoplay]" :autoplay="true" :speed="3000">
            <!-- SLIDE 1 -->
            <swiper-slide class="swiper-slide flex items-center overflow-hidden">
                <div class="slide-inner absolute start-0 top-0 w-full h-full flex items-center overflow-hidden">
                    <!-- Image Background -->
                    <div class="absolute inset-0 bg-center bg-cover bg-no-repeat"
                        :style="{ backgroundImage: `url(${heroBg1})` }"></div>


                    <!-- Overlay for text readability -->
                    <div class="absolute inset-0 bg-gradient-to-b from-black/20 via-black/30 to-black/50"></div>

                    <div class="container relative md:mt-16">
                        <div class="grid grid-cols-1">
                            <div class="text-center">
                                <h1
                                    class="font-bold text-white lg:leading-normal leading-normal text-4xl lg:text-5xl mb-5">
                                    Building Bridges, <br> Empowering Communities
                                </h1>
                                <p class="text-white/70 text-lg max-w-xl mx-auto">
                                    Supporting immigrants' integration, preserving Wolayta culture, and promoting human
                                    rights through solidarity and action.
                                </p>
                                <div class="mt-6">
                                    <NuxtLink to="/contactus"
                                        class="h-12 px-6 tracking-wide inline-flex items-center justify-center font-medium rounded-md bg-primary text-white">
                                        Contact Us <i class="mdi mdi-arrow-right align-middle ms-1"></i>
                                    </NuxtLink>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Curved Bottom Divider -->
                    <div class="absolute bottom-0 left-0 w-full overflow-hidden leading-none">
                        <svg class="relative block w-full h-24" xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 1440 150" preserveAspectRatio="none">
                            <path fill="white"
                                d="M0,150L80,128.7C160,107,320,43,480,37.3C640,32,800,85,960,96C1120,107,1280,75,1360,58.7L1440,43L1440,150L1360,150C1280,150,1120,150,960,150C800,150,640,150,480,150C320,150,160,150,80,150L0,150Z">
                            </path>
                        </svg>
                    </div>
                </div>
            </swiper-slide>

            <!-- SLIDE 2 -->
            <swiper-slide class="swiper-slide flex items-center overflow-hidden">
                <div class="slide-inner absolute start-0 top-0 w-full h-full flex items-center overflow-hidden">
                    <!-- Image Background -->
                    <div class="absolute inset-0 bg-center bg-cover bg-no-repeat"
                        :style="{ backgroundImage: `url(${heroBg2})` }"></div>


                    <!-- Overlay for text readability -->
                    <div class="absolute inset-0 bg-gradient-to-b from-black/25 via-black/35 to-black/55"></div>

                    <div class="container relative md:mt-16">
                        <div class="grid grid-cols-1">
                            <div class="text-center">
                                <h1
                                    class="font-bold text-white lg:leading-normal leading-normal text-4xl lg:text-5xl mb-5">
                                    A Voice for Community, <br> a Force for Change
                                </h1>
                                <p class="text-white/70 text-lg max-w-xl mx-auto">
                                    We unite Wolayta immigrants and allies worldwide to promote integration, cultural
                                    pride, humanitarian action, and human rights.
                                </p>
                                <div class="mt-6">
                                    <NuxtLink to="/aboutus"
                                        class="h-12 px-6 tracking-wide inline-flex items-center justify-center font-medium rounded-md bg-primary text-white">
                                        Learn More <i class="mdi mdi-arrow-right align-middle ms-1"></i>
                                    </NuxtLink>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Curved Bottom Divider (Flipped for smooth flow) -->
                    <div class="absolute bottom-0 left-0 w-full overflow-hidden leading-none">
                        <svg class="relative block w-full h-24" xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 1440 150" preserveAspectRatio="none">
                            <path fill="white"
                                d="M1440,150L1360,128.7C1280,107,1120,43,960,37.3C800,32,640,85,480,96C320,107,160,75,80,58.7L0,43L0,150L80,150C160,150,320,150,480,150C640,150,800,150,960,150C1120,150,1280,150,1360,150L1440,150Z">
                            </path>
                        </svg>
                    </div>
                </div>
            </swiper-slide>

            <!-- SLIDE 3 -->
            <swiper-slide class="swiper-slide flex items-center overflow-hidden">
                <div class="slide-inner absolute start-0 top-0 w-full h-full flex items-center overflow-hidden">
                    <!-- Image Background -->
                    <div class="absolute inset-0 bg-center bg-cover bg-no-repeat"
                        :style="{ backgroundImage: `url(${heroBg3})` }"></div>


                    <!-- Overlay for text readability -->
                    <div class="absolute inset-0 bg-gradient-to-b from-black/30 via-black/40 to-black/60"></div>

                    <div class="container relative md:mt-16">
                        <div class="grid grid-cols-1">
                            <div class="text-center">
                                <h1
                                    class="font-bold text-white lg:leading-normal leading-normal text-4xl lg:text-5xl mb-5">
                                    Connecting Wolayta, <br> Across Borders and Generations
                                </h1>
                                <p class="text-white/70 text-lg max-w-xl mx-auto">
                                    From the DMV to Ethiopia and beyond, we strengthen cultural ties, provide community
                                    support, and stand for justice and dignity.
                                </p>
                                <div class="mt-6">
                                    <NuxtLink to="/getinvolved"
                                        class="h-12 px-6 tracking-wide inline-flex items-center justify-center font-medium rounded-md bg-primary text-white">
                                        Get Involved <i class="mdi mdi-arrow-right align-middle ms-1"></i>
                                    </NuxtLink>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Curved Bottom Divider -->
                    <div class="absolute bottom-0 left-0 w-full overflow-hidden leading-none">
                        <svg class="relative block w-full h-24" xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 1440 150" preserveAspectRatio="none">
                            <path fill="white"
                                d="M0,150L80,128.7C160,107,320,43,480,37.3C640,32,800,85,960,96C1120,107,1280,75,1360,58.7L1440,43L1440,150L1360,150C1280,150,1120,150,960,150C800,150,640,150,480,150C320,150,160,150,80,150L0,150Z">
                            </path>
                        </svg>
                    </div>
                </div>
            </swiper-slide>
        </swiper>
    </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Autoplay } from 'swiper/modules';

import heroBg1 from '@/assets/images/gallery/ajora1.jpeg'
import heroBg2 from '@/assets/images/gallery/view2.jpeg'
import heroBg3 from '@/assets/images/gifata3.jpeg'
</script>
