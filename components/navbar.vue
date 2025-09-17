<template>
    <nav id="topnav" class="defaultscroll is-sticky" :class="tagline ? 'tagline-height' : ''">
        <div class="container relative">

            <NuxtLink v-if="navlight" class="logo" to="/">
                <span class="inline-block dark:hidden">
                    <img :src="logoDark" class="l-dark h-10" alt="" />
                    <img :src="logoLight" class="l-light h-10" alt="" />
                </span>
                <img :src="logoLight" class="hidden dark:inline-block h-10" alt="" />
            </NuxtLink>

            <NuxtLink v-if="!navlight" class="logo" to="/">
                <img :src="logoDark" class="inline-block dark:hidden h-10" alt="" />
                <img :src="logoLight" class="hidden dark:inline-block h-10" alt="" />
            </NuxtLink>

            <div class="menu-extras">
                <div class="menu-item">
                    <NuxtLink :to="[]" class="navbar-toggle" :class="toggle ? 'open' : ''" id="isToggle"
                        @click="toggleMenu">
                        <div class="lines">
                            <span></span>
                            <span></span>
                            <span></span>
                        </div>
                    </NuxtLink>
                </div>
            </div>


            <div id="navigation" :class="toggle ? 'block' : 'none'">
                <ul class="navigation-menu justify-start" :class="navlight ? 'nav-light' : ''">

                    <!-- <li class="has-submenu parent-parent-menu-item"
                        :class="['/grid', '/grid-sidebar', '/list', '/list-sidebar', '/youtube-listing', '/video-listing', '/course-detail', '/course-detail-two'].includes(current) ? 'active' : ''">
                        <NuxtLink :to="[]" @click="submenu(openMenu === '/courses-item' ? '' : '/courses-item')">Courses
                        </NuxtLink><span class="menu-arrow"></span>
                        <ul class="submenu"
                            :class="['/courses-item', '/grid-item', '/list-item', '/video-item', '/detail-item'].includes(openMenu) ? 'open' : ''">
                            <li class="has-submenu parent-menu-item"
                                :class="['/grid', '/grid-sidebar'].includes(current) ? 'active' : ''">
                                <NuxtLink :to="[]" @click="submenu(openMenu === '/grid-item' ? '' : '/grid-item')"> Grid
                                    Courses </NuxtLink><span class="submenu-arrow"></span>
                                <ul class="submenu" :class="['/grid-item'].includes(openMenu) ? 'open' : ''">
                                    <li :class="current === '/grid' ? 'active' : ''">
                                        <NuxtLink to="/grid" class="sub-menu-item">Grid Listing</NuxtLink>
                                    </li>
                                    <li :class="current === '/grid-sidebar' ? 'active' : ''">
                                        <NuxtLink to="/grid-sidebar" class="sub-menu-item">Grid Sidebar </NuxtLink>
                                    </li>
                                </ul>
                            </li>
                            <li class="has-submenu parent-menu-item"
                                :class="['/list', '/list-sidebar'].includes(current) ? 'active' : ''">
                                <NuxtLink :to="[]" @click="submenu(openMenu === '/list-item' ? '' : '/list-item')"> List
                                    Courses </NuxtLink><span class="submenu-arrow"></span>
                                <ul class="submenu" :class="['/list-item'].includes(openMenu) ? 'open' : ''">
                                    <li :class="current === '/list' ? 'active' : ''">
                                        <NuxtLink to="/list" class="sub-menu-item">List Listing</NuxtLink>
                                    </li>
                                    <li :class="current === '/list-sidebar' ? 'active' : ''">
                                        <NuxtLink to="/list-sidebar" class="sub-menu-item">List Sidebar </NuxtLink>
                                    </li>
                                </ul>
                            </li>
                            <li class="has-submenu parent-menu-item"
                                :class="['/youtube-listing', '/video-listing'].includes(current) ? 'active' : ''">
                                <NuxtLink :to="[]" @click="submenu(openMenu === '/video-item' ? '' : '/video-item')">
                                    Video Courses </NuxtLink><span class="submenu-arrow"></span>
                                <ul class="submenu" :class="['/video-item'].includes(openMenu) ? 'open' : ''">
                                    <li :class="current === '/youtube-listing' ? 'active' : ''">
                                        <NuxtLink to="/youtube-listing" class="sub-menu-item">Youtube Listing</NuxtLink>
                                    </li>
                                    <li :class="current === '/video-listing' ? 'active' : ''">
                                        <NuxtLink to="/video-listing" class="sub-menu-item">Video Listing</NuxtLink>
                                    </li>
                                </ul>
                            </li>
                            <li class="has-submenu parent-menu-item"
                                :class="['/course-detail', '/course-detail-two'].includes(current) ? 'active' : ''">
                                <NuxtLink :to="[]" @click="submenu(openMenu === '/detail-item' ? '' : '/detail-item')">
                                    Courses Detail</NuxtLink><span class="submenu-arrow"></span>
                                <ul class="submenu" :class="['/detail-item'].includes(openMenu) ? 'open' : ''">
                                    <li :class="current === '/course-detail' ? 'active' : ''">
                                        <NuxtLink to="/course-detail" class="sub-menu-item">Courses Detail</NuxtLink>
                                    </li>
                                    <li :class="current === '/course-detail-two' ? 'active' : ''">
                                        <NuxtLink to="/course-detail-two" class="sub-menu-item">Courses Detail Two
                                        </NuxtLink>
                                    </li>
                                </ul>
                            </li>
                        </ul>
                    </li> -->

                    <li :class="current === '/' ? 'active' : ''">
                        <NuxtLink to="/" class="sub-menu-item">Home</NuxtLink>
                    </li>

                    <li :class="current === '/where' ? 'active' : ''">
                        <NuxtLink to="/where" class="sub-menu-item">Where We Work</NuxtLink>
                    </li>
                    <li :class="current === '/getinvolved' ? 'active' : ''">
                        <NuxtLink to="/getinvolved" class="sub-menu-item">Get Involved</NuxtLink>
                    </li>
                    <li :class="current === '/aboutus' ? 'active' : ''">
                        <NuxtLink to="/aboutus" class="sub-menu-item">About Us</NuxtLink>
                    </li>

                    <li :class="current === '/contactus' ? 'active' : ''">
                        <NuxtLink to="/contactus" class="sub-menu-item">Contact Us</NuxtLink>
                    </li>
                    <li :class="current === '/news_and_events' ? 'active' : ''">
                        <NuxtLink to="/news_and_events" class="sub-menu-item">News & Events</NuxtLink>
                    </li>
                    <li :class="current === '/gallery' ? 'active' : ''">
                        <NuxtLink to="/gallery" class="sub-menu-item">Gallery</NuxtLink>
                    </li>

                </ul>
            </div>
        </div>
    </nav>
</template>

<script setup>
import { useRoute } from 'vue-router'
import feather from 'feather-icons'

import logoDark from '@/assets/images/woga_text.png'
import logoLight from '@/assets/images/woga_light.png'
import user from '@/assets/images/team/1.jpg'
import demo1 from '@/assets/images/demos/1.png'
import demo2 from '@/assets/images/demos/2.png'
import demo3 from '@/assets/images/demos/3.png'
import demo4 from '@/assets/images/demos/4.png'
import demo5 from '@/assets/images/demos/5.png'

defineProps({
    navlight: Boolean,
    tagline: Boolean
})

const router = useRoute();
const current = ref(router.path);
const openMenu = ref('')
const toggle = ref(false);
const cart = ref(false);
const userAccount = ref(false)
const searchMenu = ref(false)

onMounted(() => {
    feather.replace();
    window.addEventListener('scroll', handleScroll);
    window.scrollTo(0, 0)
})

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll);
})

const submenu = (item) => {
    openMenu.value = item
}

const toggleMenu = () => {
    toggle.value = !toggle.value
}

const handleScroll = () => {
    const navbar = document.getElementById("topnav");
    if (
        document.body.scrollTop >= 50 ||
        document.documentElement.scrollTop >= 50
    ) {
        navbar.classList.add("nav-sticky");
    } else {
        navbar.classList.remove("nav-sticky");
    }
}
</script>
