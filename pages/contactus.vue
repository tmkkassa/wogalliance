<template>
    <div>
        <Navbar />

        <div class="container-fluid relative mt-20">
            <div class="grid grid-cols-1">
                <div class="w-full leading-[0] border-0">
                    <iframe src="https://www.google.com/maps?q=Washington,+DC+metropolitan+area&output=embed"
                        style="border:0" class="w-full h-[500px]" allowfullscreen></iframe>
                </div>
            </div>
        </div>
        <section class="relative lg:py-24 py-16">
            <div class="container relative">
                <div class="grid md:grid-cols-12 grid-cols-1 items-center gap-6">
                    <div class="lg:col-span-7 md:col-span-6">
                        <img :src="contactImg" alt="" />
                    </div>

                    <div class="lg:col-span-5 md:col-span-6">
                        <div class="lg:me-5">
                            <div class="bg-white dark:bg-slate-900 rounded-md shadow dark:shadow-gray-700 p-6">
                                <h3 class="mb-6 md:text-3xl text-2xl md:leading-normal leading-normal font-semibold">Get
                                    in touch !</h3>

                                <form>
                                    <div class="grid lg:grid-cols-12 lg:gap-6">
                                        <div class="lg:col-span-6 mb-5">
                                            <label for="name" class="font-medium">Your Name:</label>
                                            <input name="name" id="name" type="text"
                                                class="w-full py-2 px-3 border border-slate-100 dark:border-slate-800 focus:border-primary/30 dark:focus:border-primary/30 bg-transparent focus:outline-none rounded-md h-10 mt-2"
                                                placeholder="Name :" />
                                        </div>

                                        <div class="lg:col-span-6 mb-5">
                                            <label for="email" class="font-medium">Your Email:</label>
                                            <input name="email" id="email" type="email"
                                                class="w-full py-2 px-3 border border-slate-100 dark:border-slate-800 focus:border-primary/30 dark:focus:border-primary/30 bg-transparent focus:outline-none rounded-md h-10 mt-2"
                                                placeholder="Email :" />
                                        </div>
                                    </div>

                                    <div class="grid grid-cols-1">
                                        <div class="mb-5">
                                            <label for="subject" class="font-medium">Your Question:</label>
                                            <input name="subject" id="subject"
                                                class="w-full py-2 px-3 border border-slate-100 dark:border-slate-800 focus:border-primary/30 dark:focus:border-primary/30 bg-transparent focus:outline-none rounded-md h-10 mt-2"
                                                placeholder="Subject :" />
                                        </div>

                                        <div class="mb-5">
                                            <label for="comments" class="font-medium">Your Comment:</label>
                                            <textarea name="comments" id="comments"
                                                class="w-full py-2 px-3 border border-slate-100 dark:border-slate-800 focus:border-primary/30 dark:focus:border-primary/30 bg-transparent focus:outline-none rounded-md h-28 mt-2 textarea"
                                                placeholder="Message :"></textarea>
                                        </div>
                                    </div>
                                    <button type="submit" id="submit" name="send"
                                        class="h-10 px-5 tracking-wide inline-flex items-center justify-center font-medium rounded-md bg-primary text-white">Send
                                        Message</button>
                                </form>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="container relative lg:mt-24 mt-16">
                <div class="grid grid-cols-1 lg:grid-cols-3 md:grid-cols-2 gap-6">
                    <div class="text-center px-6">
                        <div
                            class="size-16 bg-primary/5 text-primary rounded-2xl flex align-middle justify-center items-center shadow-sm mx-auto">
                            <i class="iconoir-phone text-3xl"></i>
                        </div>

                        <div class="content mt-4">
                            <h5 class="text-lg font-semibold">Phone</h5>
                            <p class="text-slate-400 mt-3">Get in touch with us directly for immediate assistance and
                                support</p>

                            <div class="mt-4">
                                <a href="tel:+12408148335"
                                    class="btn btn-link text-primary hover:text-primary after:bg-primary transition duration-500">+1 (240) 814‑8335</a>
                            </div>
                        </div>
                    </div>

                    <div class="text-center px-6">
                        <div
                            class="size-16 bg-primary/5 text-primary rounded-2xl flex align-middle justify-center items-center shadow-sm mx-auto">
                            <i class="iconoir-mail text-3xl"></i>
                        </div>

                        <div class="content mt-4">
                            <h5 class="text-lg font-semibold">Email</h5>
                            <p class="text-slate-400 mt-3">Get in touch with us directly for immediate assistance and
                                support</p>

                            <div class="mt-4">
                                <a href="mailto:contact@wogalliance.com"
                                    class="btn btn-link text-primary hover:text-primary after:bg-primary transition duration-500">contact@wogalliance.com</a>
                            </div>
                        </div>
                    </div>

                    <div class="text-center px-6">
                        <div
                            class="size-16 bg-primary/5 text-primary rounded-2xl flex align-middle justify-center items-center shadow-sm mx-auto">
                            <i class="iconoir-map-pin text-3xl"></i>
                        </div>

                        <div class="content mt-4">
                            <h5 class="text-lg font-semibold">Location</h5>
                            <p class="text-slate-400 mt-3">DMV</p>

                            <div class="mt-4">
                                <NuxtLink :to="[]" data-type="iframe" @click="toggle"
                                    class="video-play-icon read-more lightbox btn btn-link text-primary hover:text-primary after:bg-primary transition duration-500">
                                    View on Google map</NuxtLink>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <Footer />

        <ScrollToTop />

        <!-- <Switcher /> -->

        <div class="fixed w-full h-[100vh] top-0 left-0 z-999" :class="open ? '' : 'hidden'"
            style="background-color: rgba(0, 0, 0, 0.5);">
            <div class="w-full h-full flex justify-center items-center">
                <div class="relative px-4 w-full max-w-2xl h-auto">
                    <button class="absolute right-0 -top-4 bg-slate-600 p-[2px] rounded z-[9999]" @click="toggle"><i
                            data-feather="x" class="text-slate-300"></i></button>
                    <div class="relative bg-white rounded-lg shadow dark:bg-gray-700">
                        <div class="flex justify-between items-start p-0">
                            <iframe width="750" height="400"
                                src="https://www.google.com/maps?q=Washington,+DC+metropolitan+area&output=embed"></iframe>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import contactImg from '@/assets/images/contact.svg'

const open = ref(false)

const toggle = () => {
    open.value = !open.value
}
</script>
