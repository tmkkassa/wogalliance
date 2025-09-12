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
